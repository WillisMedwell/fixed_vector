# fixed_vector/static_vector
A variable-size array container with fixed capacity. Header only C++ container.

## Typical Usage
It has push_back, emplace_back, push_front, emplace_front, insert, erase, and more.\
It is also compliant with all std algorithms. (except for remove/remove_if)\
Check out usage [here](https://godbolt.org/#z:OYLghAFBqd5QCxAYwPYBMCmBRdBLAF1QCcAaPECAMzwBtMA7AQwFtMQByARg9KtQYEAysib0QXACx8BBAKoBnTAAUAHpwAMvAFYTStJg1DIApACYAQuYukl9ZATwDKjdAGFUtAK4sGIMwDspK4AMngMmAByPgBGmMQgAMwAnMmkAA6oCoRODB7evv5BmdmOAmER0SxxCSlpdpgOuUIETMQE%2BT5%2BgbaY9mUMLW0EFVGx8Umptq3tnYU9CjMj4WPVE3UAlLaoXsTI7BzmieHI3lgA1CaJboTxTETEV9gmGgCCRydnmJfX4TlieAAXvEAPq0PCLJ4vd5mY4MU5eC5XNyLLCqfbpAhQt4feFfH4o9KGbEwuEIpHXMTAEiEBAsEnQgiYFjpAxM5EEACe6UYrG%2BABVSOdUSAQNlgSCCOchCTTkwFApzjRVJh0CCAG6NB6XHEBKxvdJeGLg5AgaHnC3nAD0VvOXJ5CnNlq82SM53VYi8mEl3O%2Blv9AauABFzvyrvrXv6XeFgOdMuEmcQA8nA4kQ/yAFThp0W6NutAMRYg%2BOCeIpy3B84FxahrOJCNR12x4iYKjxRj7cvJythswANmzb0bMarAiLLbbLfhfu7adHhalvYH9Zz5zzsfF3vtM67FsrIrFQK3g8jzqb53wVEnHa3vvLlcxxEvVElJ%2BHbtuxHuJF3qfTdYbM8R2rAgQU/b8k3vOcQNrN8gLdFtNWIJQwMTCCU33Ah0FFRD4hQ8CHmRAiSChFch3g2MQJBXDkO9Yik0w7CQBo/C0MI64qPo0iI3SYg8A9JkzXIi0PW8W8eXOFgQXQe4mBMABWCwZXkoM4ItTcfQkqTRCJZBCE5NThSPTTvikzcT0NY08FNVcbXnRZiC8BwSEdYT7KZVReKVPAVTVTVnOICANh1U9kxASSQR0pg9K5CAhC2CLNwgDRgr3NyTD1DLVLckDME8pNlVVDUtRICADz%2BRwAWBYgwQhLFrjDRJsHOcFFmC1d/XC7SmF0/S4oSsyjwgVqCAAOiSjYNlXDLAOTA8FCJBhkUa5qCBZH4QxmiKZNaIUZQCVSyNCgMDzQdJOWGurRriYBwiCoURtG1x7rtFlrswW6GCCqajv9LLbNtejXOOhSrEUhgMAhUQnwU1SVPcvKvPo39/Ruu7gohvKMXq2bLkU0GIfwBRofQWHYYR/L3NQu5tXLNGvuCmDMfRTBMUM0GCch4m2lJlTydyynkZRi1nox1AsdZnHpvx8GuZJsn4YFrzOLYn9y1F9zzmZ7G32lsGLEJqGeYVkMlaTFi6NVyCA2Iemgq18WWbZ36Kxlg25eNvnFbHDzlZ96jMCQ1iaZ/W2PvRzXtcl9m3cN7mYa902fcR83A7wy2Q%2Bt/0p3Qe2o%2Bd3GOdlon5cTim/YXAOg4zr9tRz%2B2mcdnWjr1zmS89uGk4XFOqaFlNkDtxmfYdiWC9b4ujYTzvy6TFXM67fYGFzoeFxHp2pfS2OPan/nk8pqiLep2uf2QMPPob4f843kGt/bnfve7/f/cP5HT41xvR%2BvgGqx66L9PH92d9ebTzNucGIqBPDnGZJiC6K8axXxjvrOOpcQF7y8hpbcRlgQX1Xggl2e5b6T2AbvR%2B6DjKYKijFWBkcm7Rxbm5OyfRmSMClNFfYCoAHII7iQxYPcJztmnCmVAPJj6PBlkGMqWFRQYK1j9QuhD47EIfrwp%2Bld%2BFTk7MIzORcJHzXIbI9yiC25EJNjPc46ibwpnuJIpiMiGByM4dvJRXcVEV3HK2ARnZrF6IlFKexhj8F4yQU40xoCLGCOTFQYgsggpGInoo0JaDZ7Pw8Ro74USYlwOvn9BRKCeG%2B1TteCJAYYjRQANaxMCUXQBJiy6gIPqkyxpTkAVKyYZOyO0mDnDYZgDhm9glAMSaQpM/JzgZhTJ0vOtCx79OMQkupSTNajPGZMrJa9m64zsiwSGNA8KriZCyNkmBkRygVKNc55xXjEGAI6JqZjwmdmgQYfYIJmkVKuTc8wA5%2BznNGt065CgHFuQOaye4xyOIGDORcj5tzmphMaYIp50VvQZMEBAGFXyvm/P%2BTcoFx1QHqlQHgdAcYXQIFeeUiAMElznFUHi/0BKiUksNAoclbyIBLi%2BbS%2BllpGXEtJaykEqKCBUuHjSulhk%2BXMrJUK6JaLOX9m5ZKxZhL%2BWZHSBSlplTcZSrjMI2VmSTz7KReyCF8oFDYoxXc0ByMkX7FFZXZGJQcgCCFBi/sWKLltFxcq4Z5xkbhCUO0B1RYnVZBdQwIU1KuUSsCTaq2/rCzxBFXPURerSi5CFAqvsSr6HHTsvyAA8kGQtkkmCcjiL87%2B8b56BuTSG0CYaM2uqweJb4kalkxp5RaOyIKjknMhYqAAkgwQ0BAh31ThYsgNSbg2pvQs6gYQoR1jond5ZCBBl2jq8OOqUkKCDdutLaGtaa61zv9k2iNQpyoMH%2BOCaqtVIQNSeP62gh6T3oTuEoBtR8F3hoGIegtxbS0sHLZW85AMP3ai/ZgH9yMaAbqjRehN%2B730qqZVWegbQpmf19a4pMqqSUtiSj4rcsijUHSNW8PtYKOS%2BmYGwUM16pGHl8dKBkuTuHKIKXaejfJvK%2BWKgFZapAZRNVFPBnyRV/LsTcIKMT2BRSD3WZLS4mU3ItgILsBglx%2BxSU6aDDQZMW6Ueoya8FbhtwMYFMx2x%2BiFPQmqVw%2B%2BLieNWf44VPyJVHgNVE08UU87tSeaE7J%2BT/mQDKY/uvNTuNNPad032fTslDPGYjP9MzhzaPXHc4xwUwoWMyIcziTjLmzE5fSVJrzwnfMKYkwm4LMmSI1fCxrK%2BMXVxxeIDpr5SXWig0GsCVLjnTOvBo6ayzfHcu2ekfZjjAzamoL9eVgT0nvMidqygZD88Gtrea%2BJkA79L7TKlDNDrmAtNdYS71uSikBvHL5iZ7K7wMugvG8tvLpHJTsaao5krziyuTYq4JxrPm5N%2Bf2y/erlWQtNbBxts%2BEc2unY0%2Bd%2BLB5IeZwgAQBAEIAC0TxRZ4vS6N8zdGeTWaY/luzbGivvD%2B0M/DvHyceehyD9b4WGnV1/UF1nu24fhYRwzGhn92so4uzp9HadaLc9KtjvHBOl7fQo09sbFn3vTdY2R2nTmQkLKW4DlbVXQvg8U8xKXwc007eq/ziHrXjui%2BOp1iXLGMeiKxzjhQ%2BOmqDyJyN1XZPeRTapzNmnc25l5O4z3ZbVvjcbc5%2BnGXBVefW7C7bxXaykfqcd6jy7kuuf0Xd/L734cGa%2B6e4yUn2WDcfYK7Nn7xX5vzMW4z6PyfY8c625btvsPU%2Bm4HiXnB8D7fI%2Bz%2BLq70lkuKSMw9tLfvK8TeZ0Hz7Uptf071y3g3Mee8m4C539CW/Qe94C4d3Bw%2Bs/Zxz91vTE%2B%2Bu3ZBOZGfw2Vfz/V8HzXX3V%2BN4j65qPm/u%2BH5302zUXNxrn33/3Z321PkiyOxFxHwvzHzzwTwLzl09wV2XjLwr0yze2rw10KzD3iW/wB0XyB1WxT0APj2l0k2Bz5yPxQHrgzzP1i0vzf1dwgkL1QOL3PkmmV0cxe37Sr2IMp2X2%2B2eAb3Dy4x/0pnAUgQPwgNN2gVigYNgPP0tCd3OAgDuw2krBSh4L4KywX0DxszfzwPrzpy/wkLMWENkL21NwmmF2izgNUOYLu10JJywLVxwOMLr1ELMPENK1ASsPAJsIC1/ioUHz8UYLOzH26l6i5FcMwNew8MEJr2py13wJqSb3yV/0EOsJt1NweRIKN23w2y0VER0RsRDzI38UcItDwCoAgG62uHOA0HOB/EaOeDnDu3ajdi8AYHBDKT6AMjLhqIDGx2iQAHc38dhQJUAXwvwjBYNzAzBsAAAlFYwtFY8KfkYgTkEcIgbpZAdhRUaY1oqgcxQwYAb4JhNgQQJYw9YneA%2BLa7AmIbXUZ/dwgPCnFIyoj/dI5zf7UBVvagsguPFJIpTsXI2g0oiCco4Q/xGCEYuohogkZo1opMdoysLooJUGXo/owY0xEY/0MY1ASYg8aYkEWY6iC4xYswZYtYjYrYnYvY1AA4o41ondU484hYqBegG4rEWk%2B4kbR4y7Z48GV494OfD4gQwwoQ2vUPUwnXQZdfNzP/YE9vW3cEwomHAAjbbxOUqo9qFQ2o%2BoxotwVEton4DokMLE6pXEvAAY2gIY6eQky0Yk0kljckyk%2BYy4iAJY1Y9YzY0MJkt0fYnpBUdkqUWYrky4nk5hW4gU9mIUpw6Im/G7A2cU4nf3aUr43A7w37cw/wxZIE0g9UvvMEzxLUtnYIkAPU1Ir7eE4eREk0lEloi00ia0%2B/I8bo/WO0h0p08mF0i0N0qYndCkuY6k302k/0hkoM3YkMlksM44jkqM70q43klhO4xMp7YUnTUU9Mx/N4hI/ggwnMrw%2BUnwxUhbLIymYsoonUgXBFCEoIvI0UYVe2JsjQzs4ELQucFKbExSXs/E4Yo00YhACYkcmY8chYycukgM8KCGWMvk7pKUYVTcqpJMi0NQvc6fQ6Wfd4xIz4/jb49/FfP43XZvFUnI582ghpTUw3bUuQ18uVEVNZD8zQ4MbQ7snEvo%2B0oC50kCoksCkkiCscqk6Cv0%2BkwMhC64lhZCpUZitCwuDC8xZw1MlLA8iU/C481/YQz/PwgEos1Uks4oh8uiyEwA9lQ03GJE9itMTi/8iwQCx0gkgS10oS90piT0qCn0iSuCh2RC2S%2B4eS2QRS6aZSrCtSu/Tcc4XHc4LgDMyUgi7Moi3M88/M/ShnSimU8y0E4Asy6iiyylVikCmyr874Di38rigCnivsly3GQS8Csk0cr0ic3ymc6S9cwQOS1ChM9C7c5Mp4yKiwTQ2K%2BKjS4nI8/QnS/U34hUtfCinuTMeiqsl8kAVZFTTEB3Hc7aZLR7Sa7A5I1KtIuagsgyv1alcZHK8LdaqLbGLagakUtSvanEPQg6mU4ikwnwrMtwU5C1aFAFWUQyqitUkyjUis5amgwAu1b0dld1b5PsbFb1QFe640z86KiqjsyhfSKqxymqvigc1yoc9yt/egIwbHEEeIaJQKNqwMiWVUVUMtVQPAFgHwH%2BWIgyXqpS/qi0Pclw%2BGSsDlCokAfgYgcY42a4K1bACAJGjYX5bgqpSwawFwwJCKgzKKo8GKuKhKrSqazw3Skkb636y1AG0wwEoyu8xis3fKkG%2B8/baGg1NFOGz1P5GWlG/1eo2yw6TG0I7Ghypy/s/mwmu0Ymg8Um4Acmym0qGm8KOmrAElUDJmlmlgNmv%2BOIzmsK7mo9A8NgFgZAc6ScxLIasaoMIUHrIanCoUO7DMTcWYjleW3GU6YRC6QeIUUWIUQeawLgQ9bCgcucQWg8EWsWmGCWk2qWmWuW%2B4xWywZWtLMXQatWiwHC%2BI16pI96o62anw3VK6/bFlNlSlaNRVOlN20q9GuyzoyKH2rkHG/2uqjqNyxqljMOiO4gKmmC6c2mlmem%2BOpgRO1mrGtOswQUzO3msq3ukMVQdmKe4a0B56twpKk8lKs846ze9Dflbe03XezVCpbNblY%2Bj2sqn8729m6%2BvG5y4C%2Bq%2B%2B4S0OxgcO8lSO6mqcySmOz%2BuOxm5mv%2By%2BjmwBrc1cEBh/TaOcbO1ATUCAWNQuKBmep/XguB7SvWma0i021BkldB0UTBt8g%2BnNI%2BtighjGiKf%2BzkEhvEsh/iihomh%2BpiJ%2Buhl%2BqOxhvy2OhmhO9h5O/R0K9KZSm0bO5kPOi6Muhe4u0u6/BeiuxKI8auo8Wu/keu1cRu/OluqBdPdugfKaSwLuwyHu/mucCBhWqwaemBvC/a1e08/WxRv1QjCGkE8LNR5ijlTFQ%2Bqy1cE%2BjW3RmI1Ogxv20hgOzaIO4c6hsmqx1%2B6OqBFhhxn%2BpxlOqhVxkGdxq0Tx3O/O3xyfCwfx8fIJ2GSusqsJ4ECJqJtyGJ5upJ1uhJsBJJzu7u8usBt/bZERsR6aCRvJqRl6mR3Ww6pBje6ELegqjbdVLB98kq/B0%2Br25owx3i4xgm0x4O8x0USxim6xhh2C9q1AOXecvVDVN5SZv6ZS3HXHSRw8lewipfeRkQ95pR8p0s1R/VN8%2BptyRp783Rv820jp2%2BtyBqqhx%2Bmh5%2BgZ2xhFpF2MfY75tF9OtxzOjxljHO7xgu9JkulZxZ5ZtGo8XHLuzZzAbZw9PZiADulJw55eRJrgw9LFnFzS6Rgp/Fow4pr6%2BfI2/6z5EpjfYG4y2203Kg%2B1y26GuDBNRdTNS5AGj1H5L1AFKl46Gl8qs%2Boh1p4F2q8hu%2Bsx1lix9l/pmx%2BFj%2B/YL%2BthpO8Z/%2BQVqZzOmCJgHdFk8INEDafLe4ayC%2Bp9FEeRp4CAD1gQTW67Q9JEgtvKFstExNQt9s9Qro8N/GwO8Fnpj05q7ymkxN8KZGCGKUcId0AEIjak9FisaZ2Z8VhZ2/CwJtiBlJtZ6VldtdzduV4EXHNdjYJVlVwyNVjV1dpePKLVl6c9ndlJs5hendjJkMfuljQe8WtwSW6W/1ietJ0BqBwyNQ5dtMp93Ch5p5t6opwl2nM2u1i26sp1%2BD1as9FNPfbUGtjtDR3B7RgFzEi%2B4h9poxzpt2lljyqFuNmFzlkdoZ5N1hxxtNlxzNjF7N4eXN/YtdotxYEt5AMt%2BqCtusydat/9XIOt1Mht%2Bojj5Ec0pMSTn7PurtwjkF4jwciFmN0ULysSnyrlwMsdxFxNKd8EGdhYudvcZSs9k5ywNd69hKW9y99dpZh9xZ0DotrJ3GFwgDlW5g4D0GUD1w766agTolt4WD7Kz58LRDhihD2dVDx1d14TltHBrRv5vd4NwFlpqhbt0F3tqN1TsjkAaF%2Bht%2BphmjzAFN%2Bjjh9mkztTFj1eNj/Nuzzj1oRwHj0Qct5fKtjD0TzpcTiAWTs01smThrjtlLyaRTiNkxnL/tzywdzT4d9%2B0dhNcd/T0SflVcqrh4y0czrg6wKz%2BJ7V457byzuz05v9x94759y54R2DG5tydznJqwTzsfbzxSXz2BoDEtMtCtTAKtN4OyKDH8FDt1%2BeDD69chO8TDsVLtE8XtC1wdc4FdHdCdF9f7wboNGL0NOL5tDtBH3dddRYLdVdPdeUA9aH49adBNQHwLH8EHt/CqPAKqUEEaZaF9OgInPF5KglwLmDoG0Lm2y2iLla2gmDIHtNDDgNhlVjvNtt5tzCbj3j5EdrpqITrHrr2SHrvr6T6X1QS0gWhThlojpl46UjkSlq8S7Thb%2BeJbydlbozy49bszljM6fZw7i9tETu6znV9GHbuzs5zcLFwDrzwJpz87sD3F57V4d7kDMDb7iDX7snv1W1L8b9KnpPRDXuFDYntniDwpxBs14l0pjDFRlALDQKMWZQtznR38vzl/ORrnwGgvtBsL23EjQl6o5L9ovRzh8XlMKb8jvpyjhN%2Bbw3d0bzH%2BBgJb4jDW/Y7HIKyx%2B34ByvkMJaWBxzWET4REYNtwKsi8tfvEDfgkVc2FVfskfEZEBgHweIayBkXf8kTfpwByTAVgBkN4BMMtL33UXGOruMPiUsBiOcconNnmy5QFhWgKwYgN3zmgu5qSCgV8iQAprRQEADqUAREDID/kJEgAogFykwBTQ9Qb%2BNAByWRBSdN%2BUnMABwHOCkDww1XQ9P6EboEDrgJAw4PJDcAMAKBfVKjPmkBi3pKo96RnnVASxgJ5Q1kdyI5CaACBVwuRBMEKC4BGY7knmItltC4CkAzApARIKQEkDVdDIEgwQFIJkGrQccRgdgYJRjBPRMsLydlKk0CQ8sTBoKMwZSm4aWD9BwAawc8hhqUpEgh6XiAmHiCF4jAWfIwUYFGiA8rBcTBVoeisFVMYkFg2esdCsFBDHBT0dPAqyFChDDIng3/j4OAB%2BC3Kxg4XsEKSZhD4huQwoYkKiHRMWMK1BMC%2BjWjpBT2UAhYjAJAAEB5iCgEWiwAyEa43kYEaLt4OqEJQABkvTAYqmwFbQ1C3wW0GYEoFZQPBP/RMBkOmFeDAovQwwZtzqGXEGhCgEgCKiWGBI0hsw7YfkzeAcAtgtATgPJF4B%2BAOAWgUgKgE4BuBrA1gYUDsD2DlVYQPAUgAQE0BHCtgZSEAPJGSCjRkgkgMwMkA0ABA%2BwAADnkgaBJAkItICcI4CSBzhnw64ZwF4AwCNA7wz4VsDgCwAYAiATbCyDoDxByAlANAISPoAJA5QRgLgFCIxFYB1Q1kTAAADU8AmAcYoWnJycA3hNAWgImBgHqtkRMQcIG0E5BcjeAZIvkoWj6KijLhvALAKBiMDiBZRpAfAC2CaCagYByovKI0B3QHArhXg%2BEVcPBAxAvwOxDwFgDFHvC%2BILAMUVsCoAGAbkLItkRyMYCWj%2BAggEQGIHYBSAZAggRQCoHUDKjdAiggwEYBQD3DLA%2BgPADEBgGQAtgwiAYJqNxyohgwpgKBmYBaK45C0iQGKlQHSCsjcxXHFpLjl4iItvMuOMQLQELGGAcgg2NMEwHQDoBiMioEsaqEMDNcYqAAdUrFdi8oTQrpLjk7GtcCAFY8EMAB0yDjhxuOAAI5eAxAXYgKLjnQAPASxfED0MgE5BdiiYTAY0KqFxwJjmaQIEtrW0HGtD7gwYMwF2IqjJi%2BgZxQcSwAhBNglxjQAwLXFyAtjOxD4hUDGAPZ78sAS4vAMhC7GeB0AyYrkPQFxzDjgJSEWgKgAbF7iGR7QOcVWMHEth0AvRGSIIGfGnAPxrKBscJUHHZBxxkEgQEHBE6ES8AxE0sdsgtCESmh1kEcVd2ID2iSSwYeSF2IUDjFCAyABAM%2BKoC5teRXYjCa2F7GwsuxEMXHL0RdAM1BxPITCR2MnGkS8IuQNEUwlEF%2BAIArgOYH4EUGhAVgVQGoHoAw7aSjJ8XBgKMAMkTBFBDQdSUMFmCeAugegGyQMDsnLBKg4wBINZKWAmSvJwwCyR5IkBbANhuwfYIFP0CnCkRyom4WQNUDgi%2BwuOPsOoKpGxgaRo0DQGlPUK4BCAP4I4F3V4AfDZRk0UgD8KhHhSERvAG0X2ESCjRgRXALgCkDMCSANAUIqqaoIuFXDopaIkABiIKlaBsReIiAEgGmJjoSRoqckfEEiB8hOAsU%2BKYlMwwXE4q1U9KVcNVDZS%2BI2ERQe6OECiBxAPoraf6LUDIjgxpAcYl%2BHSC2iypZw0gO1N4DRTC0O6MdJyRmkJSkpoYlKfJDSkZSIAHgcaQxFeEbB8pWIrYAgEf5YAEg90eEYiNIA2jEgCNAIBoHBFxTQRfwyQMkFhlBAbpKIjgF1J6lAzipIAJqWlPkjwzkgrw1GfJCkAhjOAiQSKR1NRGYjCpxwzgGYFpm3T6ZvUr4aQDInOBJAQAA)

## Download
Click [here](https://github.com/WillisMedwell/fixed_vector-static_vector/fixed_vector.hpp) to download
