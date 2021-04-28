---
description: 應用程式資訊清單
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: 應用程式資訊清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c52b8eb2af87c271151be3d7989f50b2903084
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088586"
---
# <a name="application-manifest"></a>應用程式資訊清單

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-Windows 7  
**伺服器** -Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -低  





## <a name="description"></a>Description

Windows 7 在名為「相容性」的應用程式資訊清單中引進了新的區段。 本節可協助 Windows 判斷應用程式設計成目標的 Windows 版本，並讓 Windows 根據應用程式的目標 Windows 版本提供應用程式預期的行為。

相容性區段可讓 Windows 將新的行為提供給新開發人員建立的軟體，同時維持現有軟體的相容性。 本節也可協助 Windows 在未來的 Windows 版本中提供更佳的相容性。 例如，在 [相容性] 區段中宣告僅支援 Windows 7 的應用程式將會在未來的 Windows 版本中繼續收到 Windows 7 行為。

## <a name="manifestation-of-change"></a>變更的表現

在其資訊清單中沒有相容性區段的應用程式，預設會在 Windows 7 和未來的 Windows 版本上收到 Windows Vista 行為。 請注意，Windows XP 和 Windows Vista 會忽略此資訊清單區段，而不會對它們產生任何影響。

下列 Windows 元件會根據 Windows 7 的相容性區段提供分歧的行為：

**RPC 預設執行緒集區**

-   **Windows 7：** 為了改善擴充性並減少執行緒計數，RPC (預設集區) 切換至 NT 執行緒集區。 針對 Windows Vista，RPC 使用私用執行緒集區。
    -   針對針對 Win7 編譯的二進位檔，會使用預設集區
    -   如果在 \_ 呼叫任何 RPC API 之前呼叫 I RpcMgmtEnableDedicatedThreadPool，則會使用私用執行緒集區 (Vista 行為) 
    -   如果在 \_ RPC 呼叫之後呼叫 I RpcMgmtEnableDedicatedThreadPool，則會使用預設集區，I \_ RpcMgmtEnableDedicatedThreadPool 會傳回錯誤1764，且不支援要求的作業
-   **Windows Vista (預設) ：** 針對 Windows Vista 和以下所編譯的二進位檔，會使用私用集區。

**DirectDraw 鎖定**

-   **Windows 7：** 針對 Windows 7 所顯示的應用程式無法呼叫 DDRAW 中的鎖定 API 來鎖定主要桌面影片緩衝區。 這樣做會導致錯誤，而且會傳回主要複本的 **Null** 指標。 即使桌面視窗管理員組合未開啟，仍會強制執行此行為。 與 Windows 7 相容的應用程式不能鎖定主要影片緩衝區來呈現。
-   **Windows Vista (預設) ：** 應用程式將能夠在主要影片緩衝區上取得鎖定，因為繼承應用程式相依于此行為。 執行應用程式會關閉桌面視窗管理員。

**DirectDraw 位區塊傳輸 (Blt) 至主要未裁剪視窗**

-   **Windows 7：** 針對 Windows 7 所顯示的應用程式無法在沒有剪切視窗的情況下，執行 Blt 的主要桌面影片緩衝區。 這樣做會導致錯誤，而且不會轉譯 Blt 區域。 即使您沒有開啟桌面視窗管理員組合，Windows 仍會強制執行此行為。 與 Windows 7 相容的應用程式必須 Blt 至剪輯視窗。
-   **Windows Vista (預設) ：** 應用程式必須能夠在不使用裁剪視窗的情況下 Blt 至主應用程式，因為繼承應用程式相依于此行為。 執行此應用程式會關閉桌面視窗管理員。

**GetOverlappedResult API**

-   **Windows 7：** 解決競爭條件，其中使用 GetOverlappedResult 的多執行緒應用程式可以在不重設重迭結構中的事件的情況下傳回，而導致下一次呼叫此函式傳回過早。
-   **Windows Vista (預設) ：** 針對應用程式可能相依的競爭條件提供行為。 如果應用程式想要在 Windows 7 行為之前避免此競爭情形，應等候重迭的事件，並在收到信號時呼叫 GetOverlappedResult，並使用 bWait = = **FALSE**。

**程式相容性助理 (PCA)**

-   **Windows 7：** 具有相容性區段的應用程式不會取得 PCA 的風險降低。
-   **Windows Vista (預設) ：** 在某些特定情況下無法正確安裝或損毀的應用程式，將會降低 PCA 的風險。 如需詳細資訊，請參閱參考一節。

## <a name="leveraging-feature-capabilities"></a>運用功能功能

使用作業系統支援的最新相容性資訊來更新應用程式資訊清單。 本節描述資訊清單的新增專案：

-   **命名空間：** 相容性。 v1 (xmlns = "urn：架構-microsoft-com：相容性 v1" >) 

-   **區段名稱：** (新區段的相容性) 

-   **SupportedOS：** 支援的作業系統 GUID-對應至受支援作業系統的 Guid 如下：

    -   適用于 Windows Vista 的 {e2011457-1546-43c5-a5fe-008deee3d3f0}：這是 switchback 內容的預設值。
    -   適用于 Windows 7 的 {35138b9a-5d96-4fbd-8e2d-a2440225f93a}：在應用程式資訊清單中設定此值的應用程式會取得 Windows 7 行為。

    > [!Note]  
    > Microsoft 會視需要產生並張貼未來 Windows 版本的 Guid。

     

以下是更新的資訊清單範例。

> [!Note]  
> 應用程式資訊清單中的屬性和標記名稱會區分大小寫。

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



在上述範例中，為這兩個作業系統新增 Guid 的值是提供下層支援。 同時支援這兩個平臺的應用程式不需要個別的資訊清單。

## <a name="compatibility-performance-reliability-and-usability-testing"></a>相容性、效能、可靠性和可用性測試

1.  使用新的相容性區段測試應用程式，並 `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` 確保應用程式能正常運作，並使用最新的 Windows 7 行為
2.  使用新的相容性區段測試應用程式，並 `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (或完全沒有本節) ，以確保應用程式在 windows 7 上使用 Windows Vista 行為正常運作

## <a name="known-issues"></a>已知問題

**內容不相符** 應用程式會在 Windows Vista 內容中執行，而不是在執行 Windows 7 或 Windows Server 2008 R2 x64 版本的電腦上的 Windows 7 內容中執行。

**解決方案** 所有支援的 x64 版本的 Windows 7 和 Windows Server 2008 R2，以及所有支援的 Itanium 架構版本的 Windows Server 2008 R2 都有更新可修正此錯誤。 移至 KB 978637 的 Microsoft 支援服務頁面 [：應用程式會在 Windows Vista 內容中執行，而不是在執行 windows 7 或 Windows Server 2008 R2 x64 版本的電腦上的 windows 7 內容中執行](https://support.microsoft.com/kb/978637) ，以取得其他詳細資料，並下載您系統的正確版本。

**封鎖損毀傾印診斷**

**解決方案** 移至 KB 976038 的 Microsoft 支援服務頁面 [：在64位版本的 Windows 中執行的應用程式](https://support.microsoft.com/kb/976038) 所擲回的例外狀況會被忽略，以取得其他詳細資料。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [**QueryActCtxW 函式**](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   [UAC 資訊清單](/previous-versions/bb756929(v=msdn.10))
-   [Windows 應用程式的應用程式資訊清單](../sbscs/application-manifests.md)
-   [桌面視窗管理員 (DWM) ](../dwm/dwm-overview.md)
-   [內容不相符更新](https://support.microsoft.com/kb/978637)

 

 
