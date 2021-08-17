---
description: 網路監視器使用 DllMain 匯出函式來識別剖析器是否存在，以及釋放網路監視器用來儲存剖析器相關資訊的資源。
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: 執行 DllMain 剖析器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb79ab862c64d8d99359965fec6c0d1ca8bf3cf9e35fdf58f1cbc063d5c3e6c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132937"
---
# <a name="implementing-dllmain-parser"></a>執行 DllMain 剖析器

網路監視器使用 **DllMain** 匯出函式來識別剖析器是否存在，以及釋放網路監視器用來儲存剖析器相關資訊的資源。

當網路監視器第一次呼叫 **DllMain** 時，剖析器 DLL 會呼叫 [**CreateProtocol**](createprotocol.md) 來執行下列動作：

-   指定剖析器偵測的通訊協定。
-   針對網路監視器呼叫的其餘剖析器匯出函數提供進入點。

當網路監視器上次呼叫 **dllmain** 時， **Dllmain** 會呼叫 [**DestroyProtocol**](destroyprotocol.md) ，釋放網路監視器用來儲存剖析器相關資訊的所有資源。

下列程式識別執行 **DllMain** 所需的步驟。

**若要執行 DllMain**

1.  指定 [**CreateProtocol**](createprotocol.md)函數和全域附加變數的 [**e**](entrypoints.md)結構。 Attach 變數用來追蹤正在執行的通訊協定實例數目。
2.  查看作業系統所設定的 *命令* 參數值。

    如果 *命令* 參數設定為 DLL \_ 進程 \_ 附加且附加為0，則呼叫 [**CreateProtocol**](createprotocol.md) 以提供下列匯出函數的通訊協定名稱和進入點。

    -   **註冊**
    -   **取消註冊**
    -   **RecognizeFrame**
    -   **AttachProperties**
    -   只有網路監視器將會顯示) 的通訊協定屬性時，才需要 **FormatProperties** (。

    如果 *命令* 參數設定為 DLL 進程卸 \_ \_ 離且附加為0，則使用 [**CreateProtocol**](createprotocol.md)傳回的實例控制碼來呼叫 [**DestroyProtocol**](destroyprotocol.md) 。

3.  傳回 **true** ，因為 **DllMain** 剖析器函式必須一律傳回 **true**。

以下是 **DllMain** 的基本執行。 此程式碼範例會使用 case 語句來設陷 *命令* 參數的值，以判斷是否應該呼叫 [**CreateProtocol**](createprotocol.md) 或 [**DestroyProtocol**](destroyprotocol.md) 。

``` syntax
#include <windows.h>

// Entry point structure for parser export functions and global
// Attach variable.
ENTRYPOINTS EntryPoints =
{
  Register,
  Deregister,
  RecognizeFrame,
  AttachProperties,
  FormatProperties
};

DWORD Attached = 0; 

BOOL WINAPI DllMain(HANDLE hInstance, ULONG Command, LPVOID Reserved)
{
  switch(Command)
  {
  // Call CreateProtocol.
  case DLL_PROCESS_ATTACH:
       // Loading parser DLL.
       if(Attached == 0)
       {
         hProtocol = CreateProtocol( "ProtocolName",
                                     &EntryPoints,
                                     ENTRYPOINTS_SIZE);
       }
       Attached++;
       break;
  // Call DestroyProtocol.
  case DLL_PROCESS_DETACH:
       // Unloading parser DLL.
       Attached--;
       if(Attached == 0)
       {
         DestroyProtocol( hProtocol);
       }
       break;
  }
  return TRUE;
}
```

 

 



