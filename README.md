# fixed_vector/static_vector
A variable-size array container with fixed capacity. Header only C++ container. It is designed to be compatible with other std::containers and follows their conventions. 

## Data Structure Info
The following functions just increment the end pointer and do a size check. <br>
*no heap or copying here making it better than vector.*
 - push_back()
 - emplace_back() 
 - pop_back()

The following functions copy all elements backwards to make room for an element. <br>
*see 'fixed-deque' / 'static-deque' / 'shifty-vector' for a more ideal data structure*
 - insert() 
 - emplace()
 - push_front() 
 - emplace_front()
 - pop_front()

It is also compliant with most **std algorithms & ranges**

## Usage
The following is partly seudo code demonstrating how to use the header. 
``` C++
#include "fixed_vector.hpp"

int main()
{
    // Know we don't need more than 50 messages.
    constexpr auto max_messages = 50;

    // Allocated contigious stack memory for our messages.
    auto messages = std::fixed_vector<messages_t, max_messages>{};

    // Do our standard operations as if they were dynamic.
    messages.emplace_back(message1);
    messages.pop_front();
    messages.insert(messages.begin()+1);

    // Most algorithm & ranges are supported.
    std::ranges::sort(messages, pred);
    std::for_each(messages.begin(), messages.end(), print);
    
    // Reap the benefits.
}   
/*
    Not once did we dynmically allocate any memory! 
    This is the purpose & aim of this header.
*/
```

Seem more features and their usage at the bottom of [this goldbolt preview](https://godbolt.org/#z:OYLghAFBqd5QCxAYwPYBMCmBRdBLAF1QCcAaPECAM1QDsCBlZAQwBtMQBGAFlJvoCqAZ0wAFAB4gA5AAYppAFZdSrZrVDIApACYAQjt2kR7ZATx1KmWugDCqVgFcAtrRABmAOykr6ADJ5aTAA5ZwAjTGJ3AA4o0gAHVCFCc1o7Rxd3LwSkszp/QJCncMi3GKNME1zaBgJmYgI051dPcsqUmrqCfOCwiOjYoVr6xoyWwc7uwuL%2BgEojVAdiZA4pHTcA5EcsAGpNNxtCCOYiYj3sTRkAQTWNrcxd/YDktjwALwiAfVY8QbOL6%2B061omwcOz2NkGWHEyziBD%2BVxuwLuDwhcTU8IBQJBYP2bGAJEICCcGP%2BBEwTjiqjJ4IIAE84lZmE57gAVUjbSEgEBJd4fAjbBgYzbMIRCbZUPDiTDoD4AN0wphIuwRHn0VziDlC32QIH%2B2312wA9IbtnSGUI9QaHEl1NtZWwHJg%2BfT7ga3e69gARbYsvZqy5u60BYDbBIBMnEd1Rj1ub0sgBUfst%2BqDtrQtEGHzD9Ai0YNXu26cGPsTbn9gZtIeImCoESsyzzUYLvu0ADYk1cK8HC3RM9Xa9Xga6m7Gexn%2BS322Xk9tUyGeU6zcPG/qC5zuW9Fx2A1bK9t8FQB/XFy68wXYcQD1Q%2Bduu7bDsRjkqV27m6Xy7vu0WCB8H0/I2eo7fiWt6fra1bysQIi/hG/7RmuBDoFyEERNBf4nOC6EkH806dmBIbfh8KFQU6WGRghSEgMRaGwRh%2ByEWROH%2BnExB4PaZK6nh%2Br2o4J4MtsTgfOgxzMJoACsuiCmJnqgfqC7OvxgksGiyCELSskcpuCn3IJC7bhqWp4DqM7GmOgzEA4ipQTO36YOILHipK0pygqJwQDMyo7lGIACR8ynMKpdIQAwcy%2BQuEAyB5q5cbsqqaB4MkxbZ9mRhKUoyvKVkQOuTxmC87zEF8PxwvsvpuNg2zfIMHkzm6PlKcwKlqcFoW6ZuEBVQQAB04UzDMM7xR%2BUbrkIaK0OCZUVQQFIPN6g2%2BcJtTsoKCUaW665oHEtIdcVXXhMAATueynVdT4R2mhSe2YAdtDuf1uFebFiWPaZZEWjF4n6BJtAYD8LCXuJMnSWZZIpdsZEvm6%2B2HR5P12TCJVDbsEmfT9%2BBCP96CA4DIN2Q5DG0c%2B0bQ7dHnAXD0KYLCGmfajv0Y3UWPSTjyUORDkP6mdsOoPDVOIwNKPffTmPY8DrORgTRwnI2XMg9sFMI7eAtfboaN/YzoveuL2zUaRhMAe6xAk%2B58s85T1MPa%2Bguq8LGvM2Lvag/jjtEZgkE0VLSpG9dMNywrfM09basMwD9ta47eORrrMGewbbqDugJv%2BxbSO00L6Mi2HuNg4R0cQwnJvk2bisPcrdMZ3bQPh%2BOkcgzHj7S3myDG2Tjum7zKdl%2Bn6uh1X2fO%2BO9dwU3stFx3/MfUHtu9yzEc5y7ef64W3s3YXbfJxPj1pzbFczw7Nfz4Pi%2Bx8vo/r8XAelzFpn%2BYF6mTyrweZ332uhKg9jbOSsLba347t%2Bbm8raP2nkzF%2Bc8HLySXJpd4a8/4b0DsA3eoDZ4HwgVpKBt9mq/2LPAq%2BL0TQVHJFYfkAVliii7jvHuyD96DFrv2OsQ5oyoAZA3bCgtPTZUQlySB8t7qpynkgzW/cJYLxrAwhszDY5pw4SNdBvCQYIPLlQoR2t6GDgbFGY4nDKI8NoHwihT9K4oNoYfPsYj1H3C0bI3k/I9EKMtvmARyis6qPMceaMVBiB0AIO5RR3cQ7UOriYgeZijyMM8d42BvwHGricQElR4Co5uMYVGUIAUADWviYnI0Qc4sBqCRFH2SQ2NJyBMnYMAQaUyi1mDbFIZgchD8lHxJcYkn02x4zRhqUnC%2Bncmn%2BOfsYp2hTiwsg6fuESUTbG9MqfqUyThfoSlQjOMkFIqSYHBMKUUXUdnbEuMQYAFpyrCJ1sU%2B4X9VDLA%2BKUzJ%2BzDk6HbG2HZXU6kHKEPomKqzKTHA2fRVQ2zdl3KORVVxYSGwXICk6CJ9AIBAoeQ855rzDkfMetrWUqA8DoFDNaBA1yMkQGApObY4gUVujRRirFGohC4puRAScDziWkoNOSzF2LqUfGhT4wlDKSUaRZZSnFHKvEwvpW2RlfK2notZQkOIeKylZKRvy0MzChWRJRSsiF1I/kiiEIiuFxztYQwhcsAlLsIbZGSHQdkcK2wIt2XUZFEqCngyXgEEQ9RTWD3NYkS1tB2TcrFby7JhrXUZgiFys1S8LVVHZKK1s4q8FulMiyAA8p6FNAlmC0nCM8kyJoQ0nzdeGz1mZvU5BSOySBp4/VyyJUGpGpkvnrM2f8sUABJWgGoCBtpKiCtpEMi0eslqwyM0aK3bA7V2ntjkoIEHZJOhw3b%2BT/IIEyuZ%2Bb%2B2hvdRGr1UafUxo5FwkAuU8D5U%2BJ1CaZxwasDXSco1j4RAlp/GW31t7k1pozU4LNOadl5oLSOz%2BD7MBPqHtLCUs7/WRpPiu29SrNiYDqD08eTrgmRilVi6s4VrGLl4dueKMk8FNp%2BTSF0tAmSskrUenhgpyr/G3oYveQThmmlI%2BRxy6UXJWQmqQGj2AuQQzSs5TKdEbBsl41yFu/8EaxSRtWAgixaC7DbIJGpn0ZDY1LqtK4RGtU2CXGR5kPpKM6LkbxujcTBk0OY/ptjgmMquWwqVHjZwuTDrgnZzjImxMuZAJJseACZMzjkwppTrYVMiTUxp/0%2BHSSat%2BXp1jhm2SHpMzYgUJILNGKs7XGzhmPPCcc6J5z5V%2BNL3yw504TnxMgFlhvQLMVgvEEUw88LtRPptXeFFujWnLg6fi7lijKXuGmYy7klp%2BTUMsYZAZ%2B45WuNVZ825sDTl7PzaK9Vs%2BcCZn1ceo15rymhIRYkh1jZzNNPPVi2s4j%2BwBtGaGxuNLZmESZcYyc27c2vPFb41RN2qE9Ynw%2B4V7zJWqKSbq4NILmB5NNfu8fEdEACAIB%2BAAWjOFzdVPW%2Bskem2x5L2G%2BTpdo89sblmmM5cS7Nlbnmgdfdc6I92/2AOA8q%2BtnzK9fb%2BekxDhrUOQvrjh/%2BBHSOhCo/KujvDmO4vY8ZEl4zw3HujeaaTt7FP2NCYq9x6rAvlscYKyz4H32C7c3Hjt%2BOvOYf89%2ByRUDJAhco7OC3DHz0sc3dV3jqjI2ifXBe4ElXOO8tU715rxb9O/s29SoHjXC2QdG79tt7nu3zeKctwz8PduRcO59qTJ3dHtNS9d/7wb%2BP%2BRPe9yTrLZOwbvcj2tg3dPd0A5r596rzcs9TKk3zU3Bo9uhda6JCS6mzvRcl1d3Tt33epZw6X%2BjICEnOur7rqPrOQdLaVMz4PK/Ns4Pj3FHn0P9thcO2147Hw9JD%2B687/PCXC93eL4T84xOlcV79zLyni/a%2B05QKH63Amm805b%2BzqTHHibgnmbvvrDlbh7PDojvbmLtYHdBLpfqPv1m7nLg9lPorgMs/trAvurh/i3t/lAe5n/vrp/sgLHpzp3qAd3knhAanmROnqLtgI7ogbnr1lfuPmgdRpgZQuNkMrXG/B/OvtHt9l/EFBUh3rCF3vqD3hACdrNAWJFKwXnsgdLjNrfh7grl7jPoIq0s6nfsIcvt9r1MAQFtQTIbQSdsoewaoQXq/hoZPgTtPj7nPpNgYSQRvt9pguIaYVzrvonuAQ1E1HSNYZdt8mPqgfdtwdoS4XoZNrgats3mzmcmrokf/j5pIiOtItovLjhnYuYeDFQBAM1vsNsDINsEqCUecKOCdjVNbA4LQN8OkhUOpFnAUW6Ijl4gAO73YLA/ioDXiPjqDAY6DaDYAABK4xKa4xPkLIxAtI3YRAdSyAZCYofRFRVAOsagwA5y7AzI9Aoxt6MWe%2BIWfeqMXWKoSB4RKBN%2BE%2BuRThPBDGvuOBquhhdeX%2BRSYKb%2BeBSRIOmR/42Rd%2BdiwEBReARRJRNgZRFRkYVRBYtROSn0DRTRLRQi7RBonRqAPR64fRHwAxRE2xIx2gYxkx0xsx8xixqAyxqxFRi6GxWxwxn8exxChxNMPWYBpxR%2B/eqsFx1wI%2B1xahuOXBnuD%2BZeT%2Br2LxN%2Bbxn%2Bai7iUp1WVimheRNU/hboYJxRKIUJlRDw1R3o8J28SJeAzRrArRfcaJ%2BoGJWJR6OJeJQxOxEAoxExUxMxPo5JtoSx9SooNJ/IAx9JOxjJRCBxRJRxbJNBgRnJ5x5%2BlxYRzadh6hdx6BDxMR5e4pbSCR1OpBBBnx4i3xaRGZPmCpjhtiEhoJ4JGp5RWpOEupp%2Bm4dRKsBpRpJpOMZppoCA3RvRi6uJgxBJ9pRJjppJLpCxbplJHpaxtJPptpuxAZcIQZrJz07JMOZx30PJxxNh/JsZgpURwp5myZzxqZrxHhIhyEKRcpPmnKJsJZch1Z7wCho4kUCJEk9ZKJbRKp0YFp7Z/RXZwxPZxJTpPkP0/p%2BxJC/InKLJ2SK585imi5ugg%2BBGw%2BVxMZ1%2B9h8Z0RIpOheS/BVe%2B57%2BvxXhoiXxqR6ZnhXIZ5xZL5%2Boap8hXoihtZiJjRhpT5ppZF7ob52JHZNp3ZDpJJzp/5hCgFdSwFwq052gwZc5oZHJqmA%2By5fJCFnBm5WhqFsRE21mWFPx6RMex5B5RhEm%2BKypSMFFV59wVFt5NFD5dFDZqJTFHRrZmJ75nZ%2BJX5nFv5psAFxC/F4ogloFqcIZFhYZElug8hyO2wnAUl8F12iFcZQp8l25Ypu58%2BKluZRFHxoS2ZBFQeh5vmOlcsF5lFsY1F95ugj5xpFlSMVlbZrFH59ldpjl/ZPFTJ9AblIFM5YF3lpyvlR2/lBl2wgVwVkZvJF2Kha54VG5d%2BzhO5rhzGCYqVS%2B7x3SxuZhTFPeZx520ZYVslI1jxs%2BcRzGhKnSJ5IOs1vhVBC1lh4Zy1CIA1MlkR61XuLuNgWyuqgKbyQoe5kpml7xMp4Sb1n%2BxqTotKNqjyrYiKDq7y0hhRl5C4N5VZ3htIJlBVZlDFTZll6J1llplE7A6giOHwEQXixA35fZzpvM0o0oma4geATgzghYjUAUaknlA0LVUFVhwMBYdKORIANAxAXRGs%2Bw%2Bq2AEAwNMwzyfUNMegBgVh2Si14ZJ%2BEN3VIVK1ERtxkVGBN1V%2B91eqT1XuEp9he1huGl2FalohV2VyZ5/1dqLy/NoN%2BlENRlUNVNd8sNhVjZTNSN5pKN926NwAmN2Ntu1VBNlMRNWKX6pN5NTglNwR6kTVXlol6664zITgyAW0PZh%2BflPVno7ILWkt0FgM7IJ28YC4AxdKQt2SG0zC20Lc7IXM7ILcBgnAt6UFMFs02wLN647NnNAM3N6tvN/NgtRxItegYt0WJxC5GdMFoRF1q1V1ipiZIpSq2tXIVKNK%2BKAa8aJKFtRROVBGNtYd9t8NRVz5JVyNZVR67tntxAONeNXFPkhNWAAdzAQdFN0NtNH09NGdjNc0o44gwt%2BgfdBl1ht1a1k9Jez1zq6GU1%2BBPm89cqmScajKq94Nm4kNvk0N29yJu9jF%2B9Lth9aNVgHtuKXtuNPtl9ft19JNZN99ttNNEddNUdC07Vr9DdMdqA8oEA9aA0vdHVekZ11wY98tSFitU9/wM9X11WEDZ5S9MD2VnV1tiD5DdIyD9FqDiN6DLZmDXIx9uDp93tvZF9n8RDxNgdpDIdD9lDT91DxoMd5I8d206dydWdvew9tjOdedRRLIhdSMxdCdZdn88BoUVdegNdGkddTZ79n9otP9nDf9E9hZ9%2BAjkqFKoDOFc9gqZ50DK9EjVtuVNRfkMjMN%2BVDtxVtUB9Nl64ajWNGj%2BDWjTlV9ejt9Bjod1NIRxjW8LVZjR6sdljidUFKdadB2flMF2dBludm4%2BdLjt67jpdbeoUFd2wvjug/j2SgTTNo4DDTDLDH0bD/dF%2BbBETCtclSt09sTrKs9IAMqkD55TFlt8DUjd5%2BpO9jtc0ztyjRTR92DJ9Z9BDpsMBQ5yqsqNyj9TT1DyOyOGzUZ3DNxvDuz/DVwgjeteZIOJzJFsD69eVNzKDdzoNpVTzWDGN6jbzFTNVqAnzIYSxJzvzjTr4zTho5jcdCd1j7VfTdjNj0k7IcD7wyONdgz7wwzrjM4YzEAMznA5d3jldEzt6gLwLfVbBctYLEVELgDytthd1raat9yGtL1WtQjPmv%2BMLiVP1IGL6B6JtTy9qbyulM4Fz15UjQR9TOTKL8jaLzZLFzz2LpTuLP5/ZVTN9d9hj2Tfz5L1DwEzAi6lJAQUI9DtQZgyAWT0SEIADZwEAY6dAXVNDtQt6apIbdkZZ0J4M1gGbV6LLmAfUuTtz%2BTMUGLqNXI1pn5VVeLzpEMP0/IAQdoLwGGBJvr%2BYFLVL7TtLx%2Bug6bH9fjtj3bXJfbtj%2BbyOfbMwHLmAXLozR6m04zq8/UegfbgricPjEzBgI7fjtdGdI7iz3oTdR6LdXNNgPNfNJr3dATP9bDGkPeQ7n0e7sFmzoLApsusr0TULar6hRzWrqlsL32g6O6pae65aVqtaPKprMU5rhlGTm91rcj5le9BTGDmLqjLzOLmjbrvtyw/tJDwddTd8bbq4LVAbQb2bobCExwRkUbJUMbhZcbCbimgVfeqbRRfbmbSo7HebtRCHCNTtSjjrlElblVhJWHPkdbBL2bTb3wLbwxRHT0PLc7JdfLG7y7Ob4gq750MzW7szO7flj7DdH98z17X9%2Bg4ttB97Ekj7v9HBkT9xcr%2BzcVr12r6Vv7CVrnYaQ6UGAGjHsa8KgakHj00HCDVrdtRbqLJbj0Zbbt6HLrmH%2BNhDOHxD%2Bj%2BHRjwls5NkbcgbSxXHSz4b1HLA0bxeDH%2B6KQSbLHGkab6nHHkYuXFU%2BbhbtriHaDyHjz5bIAwnE559TlEnDbimPErKE58n4FBovL2n6nmn67i7m76n1den7VBnFEXICyKzO7ekN75n4Blnvbs3vVK5766ama2amAuaVwN8m6hannQHz6IHvqla6C1akGf8daKKjaKtraE6nai6PaV6/6cEgHert3B6C6S6M6gw86X3oPMG2453zqA6V3gPJ8vn92J6Z6hUF6pUV6eAN6eGL765b711jn8R8VhFrnZWGrIORwj6q%2Bo6pXdAgXZKWXZHuX3o4wEbNH4IxX5U8bdPTHybzArHEAuXkJ5ZtX1XlZjdPH4XdrkXeYgnFbbFVbonCXLqJ89bUnA3snOxw3LVY3qnO3UI1dk3wr03anUIa3m4gLt7FnPTC3u3T7ILXDlwB3n636J3v6Z3G6cPS8VPwGNPYPc6dcEM0PhGtnOzhPMTwDcTRz8GiGc1fhSM69ZRNnCr/9UTpe0Lf7iVmG7UQJDPBoapVR0jW96LhT7XJTeD3X/ZdmdoFWlNtA6vOf15SxiOxwlU6HOv1DSf40nDdGgItwoIMHNgE5wKffWIyI4ItAzgEQRkJI/fSIg/KI5g5kCGxI2hVw4YmaMM3WSM2XlJLE4YuYBY2RpHRADK6YtQAQEQ%2BfUYapF/zAV/xAPU7UNUsHUJN/jYxdtJ4I4ISm2gdg9AB/oEFq5igxC4dbQGtHbbUM3QFQEQKX2GhHoR%2BxFEgFjQCgIBPUl/YAWnXYRPo6kQbBlAW3mhf9%2BQP/UokP1/5gApA2wSgX6Cei3o/WrXYgSiAoGrAxINgWgDQOaoO8neSaE0Kj2%2BAFQioxYBlGkiSDIAQYFkUwCkBnCGFww7ITgOpmOQ19j%2BqoIKqQG0CkA3ApAbgAp2ySyD6A8gxQVNCRzqBcej0A/jmFxqEtb0hLU6IbV%2Br4o5mSMWwT9VObpdskLg%2BwaczcC3oLBEYO3OoHVSfITBwALqAD1sGeMlC2SPwREACHAAghj0WwSI0EoQA2Wvg1iJYLiEJCrKwYMIQjxcFCsuqTgmcDEKsEhDshyNXIbqwKFrt2QyOdwUjFKFZCzBOQ9QKdCAxxCroi7GwSEPaEihgMNQ9yGkI0j6C50Cgq9NNDiAaR%2BcBJIQFyAIBDEhA7NJwHELQI3JfwV3WIZMNCgn8meZ/MVIQNUE957gJoCAWWDoEaQmh1gy4RkP8HbCWh6JS6PCxSE2DLorgs8goPSGH8rBFICoXJEQGzDuEJAHxPcOiG3Cthvwh4eaUuix9caXwzIaCLgr/ApAcwVgNIDEjyBXAsgeQKgGkA2ADABgDkAsCWCGVAQnAeQAQGkByA%2BopAdJCADEgABOLqAyO4DaAGRMgDwK2CiBiQZA3AbkQyJUDSBuAmIqkTiOkDyA5hMgUgJSOxFzA4AsAGAIgC/wUhseEQcgJQDQAqj2AkQYUOoE4A8ipRWAWUEZEwAAA1PAJgC6Ippps0gckXwGx4Rg5hfLUUaQFCABA6gtIW0fIE1GAUU0jRT0diNIBYAv06gdgC6PwDVgpB8oOYYGLsgKhF0KwOQOQBzBojAx3wUII%2BHmJ2AsAXo6UaxCcBei5gVAVQIcnNGWjrRVgXMfwEYAsAwxPAPgN4mEBiBJAgYpQAK1UDqAUABIvQCoDwChA5hkAOYMwiqAxjkckIL0FoDYbaByiyOEMMjioBxALRXVKgOMDKTI4WIBLCrMjjYCsBlxQgNQMkE6yxhmA6AdAJhjFDrjpQagCNl1QADqO4u8XZAWG1Jkct4wrgQG3HfBgATHN8SKA/EABHBwGwDvFWRkc6AE4OuNYj2hkAtIO8ejGYBahpQyOYcWTTeBUdE2r45YccC9DaA7xuUMcRUE2KvinAPwSsGBIVCqAG4KQC8beJImihgw47BflgDAl4AoId4%2BwOgDHF0h2AyOd8exMgisBUAJ4pCcaPqBATdxr46sOgAaLCR6A5EzYDROpQnibKr4pIN%2BN4l0B3YZXVSXgHUkbiFk%2BoVSQsKMgfjGGEQYsZiS9BiQ7xQgLooQGQAIByJVAQNqwH5CviZJNYR8WUzvE/RkcDRa0MTVfEMhZJN418emC0l0AJRhCKQRYAgA%2BARgrgAVj4EmC9BIgArRjglOUCMcUpRQPoAK2MCuR2gQwBoPYCaDKACpMU6oMVJynTB8pxUzKXVImBX8pgeUuYEIGJHLAuAqI9ESKMDG4iqB4gKIK2GRytgdBuokMPqK6gyAppjdXAIQCVBrAa6FI0UTSLpE8jBRUgYUaQALE8iuonAHgNwE4CjSPAjIjwNoDEhiRSAWIpMf1IlEgApRMo6kaQHlFKi%2BiXadUaai1ERAgg5GaQINOGmjTCwHYiaW4CmlTT5A0oeaaxCQgCtqxTANgBwHrHVimxEgF0W2NIBdFHwcQQsRtIxFXSXR/UlNIui7R0l/pI0sacDKCpiQwZ5RCAHYC%2BnkQyRMwZabKLmAIAEMWASIEdFTFbSCx3AJkTEAulRA3AYkbQNwBkDaAPA3AS6ddLFFSA7pD0laXMDpHiyppYkDwDIAZFkj%2BZYkHgO2OkBuBepN08UdKKVkbTtARsuWSzOpFzAIprgbgEAA%3D)


## Quick Download
Click [here](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/WillisMedwell/fixed_vector-static_vector/blob/main/fixed_vector.hpp) to download the header right away
