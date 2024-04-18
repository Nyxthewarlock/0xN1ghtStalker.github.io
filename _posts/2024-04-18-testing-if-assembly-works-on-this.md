---
published: true
date: 2024-04-18
title: testing if c works on this
url: 0xN1ghtStalker.github.io
---
```C++
undefined4 something_weird(void)

{
  undefined4 uVar1;
  int iVar2;
  undefined4 *mysterious_url;
  undefined4 *puVar3;
  undefined4 uStack_64;
  undefined4 uStack_60;
  undefined4 uStack_5c;
  undefined4 local_50 [14];
  undefined4 local_17;
  undefined4 local_13;
  undefined4 local_f;
  undefined4 local_b;
  undefined4 local_7;
  undefined2 local_3;
  undefined local_1;
  
  mysterious_url = (undefined4 *)s_http://www.iuqerfsodp9ifjaposdfj_004313d0;
  puVar3 = local_50;
  for (iVar2 = 0xe; iVar2 != 0; iVar2 = iVar2 + -1) {
    *puVar3 = *mysterious_url;
    mysterious_url = mysterious_url + 1;
    puVar3 = puVar3 + 1;
  }
  *(undefined *)puVar3 = *(undefined *)mysterious_url;
  local_17 = 0;
  local_13 = 0;
  local_f = 0;
  local_b = 0;
  local_7 = 0;
  local_3 = 0;
  uStack_5c = 0;
  uStack_60 = 0;
  uStack_64 = 0;
  local_1 = 0;
  uVar1 = InternetOpenA(0,1);
  iVar2 = InternetOpenUrlA(uVar1,&uStack_64,0,0,0x84000000,0);
  if (iVar2 == 0) {
    InternetCloseHandle(uVar1);
    InternetCloseHandle(0);
    FUN_00408090();
    return 0;
  }
  InternetCloseHandle(uVar1);
  InternetCloseHandle(iVar2);
  return 0;
}
```