---
description: 您是否想要在 debug 期間找出有關 Direct3D 物件的詳細資訊？ 例如，下列螢幕擷取畫面顯示當您在 [監看式] 視窗中查看 Direct3D 介面時，通常會看到的內容。
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: " (Direct3D 9) 啟用 Direct3D 調試資訊"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bb46cf8658d0417d021faa6bdbefd10822d1dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108404"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a> (Direct3D 9) 啟用 Direct3D 調試資訊

您是否想要在 debug 期間找出有關 Direct3D 物件的詳細資訊？ 例如，下列螢幕擷取畫面顯示當您在 [監看式] 視窗中查看 Direct3D 介面時，通常會看到的內容。

![[監看式] 視窗中的 direct3d 介面螢幕擷取畫面](images/d3d-debug-info1.png)

您可以啟用核心 debug 物件，以便在 [監看式] 視窗中，可以看到包含物件之所有屬性的鏡像物件。 在 \# D3D9 .h 檔案之前的程式碼中，只需包含下列定義：


```
#define D3D_DEBUG_INFO
```



若要啟用 debug 資訊， \# 必須在 D3D9 .h 檔案之前建立定義， (任何使用 DXUT 的程式，在 \_ \_ 編譯器以進行 debug) 時，會自動啟用 D3D debug 資訊。 如果您執行的是 SDK 範例，您可以在 DXStdAfx 中看到此 (，這會影響所有) 的 c + + 範例。 您也必須執行 debug Direct3D 執行時間 (如果必要) ，可以從主控台啟用。

以下是使用 [BasicHLSL 範例](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx)的範例。

1.  在 \# 37 行之前，將定義新增至 Dxstdafx .h 檔案。
2.  建立 debug 專案。
3.  在 BasicHLSL 的第307行設定中斷點
4.  執行偵錯工具。

下列螢幕擷取畫面顯示您可以從 [監看式] 視窗取得 Direct3D 材質物件的詳細資訊類型。

![[監看式] 視窗中 direct3d 材質物件的螢幕擷取畫面](images/d3d-debug-info2.png)

> [!Note]
>
> 物件屬性名稱是可見的，只有在啟用偵錯工具執行時間時，這些值才是正確的。 針對零售版執行時間執行時，值無效。

 

## <a name="use-the-call-stack-for-extended-debug"></a>使用呼叫堆疊進行擴充的偵錯工具

啟用 Direct3D debug 之後，您也可以在每次建立物件時查看呼叫堆疊。 這會讓您的應用程式變得非常緩慢，但是可以用來檢查資源流失。 若要寫出呼叫堆疊，請將下列登錄機碼設定為1：


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



使用啟用偵錯工具建立您的應用程式，可讓您存取這個額外的變數：


```
  LPCWSTR CreationCallStack;
```



此變數會在每次建立物件時儲存呼叫堆疊。 這會讓您的應用程式變得非常緩慢，但是可以用來偵測資源流失。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計秘訣](programming-tips.md)
</dt> </dl>

 

 



