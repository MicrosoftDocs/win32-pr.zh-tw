---
title: 初始化 COM 程式庫
description: 初始化 COM 程式庫
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968494"
---
# <a name="initializing-the-com-library"></a>初始化 COM 程式庫

任何使用 COM 的 Windows 程式都必須藉由呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 函數來初始化 COM 程式庫。 使用 COM 介面的每個執行緒都必須對此函式進行個別呼叫。 **CoInitializeEx** 具有下列簽章：


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



第一個參數是保留的，而且必須是 **Null**。 第二個參數指定您的程式將使用的執行緒模型。 COM 支援兩種不同的執行緒模型，也就是 *單元執行緒* 和 *多執行緒*。 如果您指定了單元執行緒，則會進行下列保證：

-   您將從單一執行緒存取每個 COM 物件;您不會在多個執行緒之間共用 COM 介面指標。
-   執行緒將會有訊息迴圈。  (查看模組1中的 [視窗訊息](window-messages.md) 。 ) 

如果其中一個條件約束不是 true，請使用多執行緒模型。 若要指定執行緒模型，請在 *dwCoInit* 參數中設定下列其中一個旗標。



| 旗標                          | 描述         |
|-------------------------------|---------------------|
| **COINIT \_ APARTMENTTHREADED** | 單元執行緒。 |
| **COINIT \_ 多執行緒**     | 多執行緒。      |



 

您必須只設定這些旗標的其中一個。 一般來說，建立視窗的執行緒應該使用 **COINIT \_ APARTMENTTHREADED** 旗標，而其他執行緒則應該使用 **COINIT \_ 多執行緒**。 不過，某些 COM 元件需要特定的執行緒模型。 MSDN 檔應該會在這種情況下告訴您。

> [!Note]  
> 實際上，即使您指定了單元執行緒，還是可以使用稱為 *封送處理* 的技巧，線上程之間共用介面。 封送處理已超出此課程模組的範圍。 重點是使用單元執行緒時，您絕不能只將介面指標複製到另一個執行緒。 如需 COM 執行緒模型的詳細資訊，請參閱 [進程、執行緒和單元](/windows/desktop/com/processes--threads--and-apartments)。

 

除了已提及的旗標之外，最好在 *dwCoInit* 參數中設定 **COINIT \_ DISABLE \_ OLE1DDE** 旗標。 設定此旗標可避免 (OLE) 1.0 （淘汰的技術）與物件連結和內嵌相關聯的額外負荷。

以下是您初始化 COM 以進行單元執行緒的方式：


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



**HRESULT** 傳回型別包含錯誤或成功碼。 在下一節中，我們將探討 COM 錯誤處理。

## <a name="uninitializing-the-com-library"></a>將 COM 程式庫取消初始化

針對每次成功呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)，您必須線上程結束之前呼叫 [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) 。 此函數不接受任何參數，而且沒有傳回值。


```C++
CoUninitialize();
```



## <a name="next"></a>下一個

[COM 中的錯誤碼](error-codes-in-com.md)

 

 