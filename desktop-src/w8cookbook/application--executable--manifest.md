---
title: 應用程式 (可執行檔) 資訊清單
description: 應用程式 (可執行檔) 資訊清單
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104024221"
---
# <a name="app-executable-manifest"></a>應用程式 (可執行檔) 資訊清單

## <a name="platforms"></a>平台

**用戶端** – Windows 8  
**伺服器** – Windows Server 2012  


## <a name="description"></a>Description

在 Windows 中導入的應用程式 (可執行檔) 資訊清單的相容性區段，可協助作業系統判斷應用程式設計為目標的 Windows 版本。 此外，應用程式資訊清單也可讓 Windows 根據應用程式目標的 Windows 版本，提供應用程式預期的行為。

資訊清單的相容性區段可讓 Windows 將新的行為提供給新建立的軟體，同時維持現有軟體的相容性。 本節可協助 Windows 在未來的 Windows 版本中提供更佳的相容性。 例如，在 [相容性] 區段中宣告 Windows 8 的應用程式在未來的 Windows 版本中，仍會繼續收到 Windows 8 的行為。

## <a name="manifestation"></a>表現

在資訊清單中沒有相容性區段的應用程式，預設會在 Windows 7 Windows 8 和未來的 Windows 版本上具有 Windows Vista 的行為。 請注意，Windows XP 和 Windows Vista 會忽略此資訊清單區段，而且對它們沒有任何影響。

這些 Windows 元件會根據相容性區段提供分歧的行為：

**遠端程序呼叫 (RPC) 預設執行緒集區**

-   Windows 8 和 Windows 7：若要改善擴充性並減少執行緒計數，請將 RPC 切換至 NT 執行緒集區 (預設集區) 。 針對 Windows Vista，RPC 使用私用執行緒集區：

    -   針對 Windows 7 和更新版本的 Windows 所編譯的二進位檔，會使用預設集區。
    -   如果在 \_ 呼叫任何 RPC API 之前呼叫 I RpcMgmtEnableDedicatedThreadPool，則會使用私用執行緒集區 (Vista 行為) 。
    -   如果在 \_ RPC 呼叫之後呼叫 I RpcMgmtEnableDedicatedThreadPool，則會使用預設集區，而我的 RpcMgmtEnableDedicatedThreadPool 會傳回 \_ 錯誤1764，且不支援要求的操作。

-   Windows Vista (預設) ：針對 Windows Vista 和舊版 Windows 編譯的二進位檔，會使用私用集區。

**DirectDraw 鎖定**

-   Windows 8 和 Windows 7：針對 Windows 7 和更新版本的作業系統所顯示的應用程式無法呼叫 DDRAW 中的鎖定 API 來鎖定主要桌面影片緩衝區;這樣做會導致錯誤，並傳回主要複本的 Null 指標。 即使桌面視窗管理員組合未開啟，仍會強制執行此行為。 針對 Windows 7 和更新版本宣告相容性的應用程式不能鎖定主要影片緩衝區來呈現。
-   Windows Vista (預設) ：應用程式可以取得主要影片緩衝區的鎖定，因為繼承應用程式相依于此行為;執行應用程式會關閉桌面視窗管理員。

**DirectDraw 位區塊傳輸 (bitblt) 至主要而不需要剪切視窗**

-   Windows 8 和 Windows 7：針對 Windows 7 和更新版本的 Windows 所顯示的應用程式，無法在沒有剪切視窗的情況下執行 bitblt 至主要桌面影片緩衝區;這樣做會導致錯誤，而且不會呈現 bitblt 區域。 即使您沒有開啟桌面視窗管理員組合，Windows 仍會強制執行此行為。 針對 Windows 7 和更新版本宣告相容性的應用程式必須執行 bitblt 至剪切視窗。
-   Windows Vista (預設) ：應用程式必須能夠在不使用裁剪視窗的情況下執行 bitblt，因為繼承應用程式相依于此行為;執行此應用程式會關閉桌面視窗管理員。

**GetOverlappedResult API**

-   Windows 8 和 Windows 7：解決競爭條件，其中使用 **GetOverlappedResult** 的多執行緒應用程式可以在不重設重迭結構中的事件的情況下傳回，而導致下一次呼叫此函式會提前傳回。
-   Windows Vista (預設) ：提供應用程式可能相依的競爭條件行為。 必須在 Windows 7 行為之前避免此競爭的應用程式應該等候重迭的事件，並在收到信號時，呼叫 GetOverlappedResult 和 bWait = = FALSE。

**高對比模式中的 Shell 主題狀態**

-   Windows 8：在高對比模式下，傳回實際的主題狀態。
-   Windows 7：因為 DWM 仍在開啟，所以在高對比模式中，會將主題傳回為無法使用。
-   Windows Vista (預設) ：在高對比模式中，因為 DWM 仍在開啟，所以會傳回無法使用的主題。

**Shell iPersistFile：： Save 方法**

-   Windows 8： CShellLink：： Save 現在會判斷是否以相對路徑引數呼叫 IPersistFile 處理常式，如果是，則會失敗。

    描述此行為的 [公開檔](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) 指出路徑引數必須是絕對路徑：

-   Windows 7 和舊版 (預設) ： CShellLink：： Save 無法判斷 iPersistFile 處理常式是否傳送相對路徑檢查，並允許應用程式繼續使用絕對或相對路徑。

**程式相容性助理 (PCA)**

-   Windows 8：具有相容性區段的應用程式不會取得 PCA 緩和措施。
-   Windows 7：此檔) 所述的 Windows 8 (變更的潛在相容性問題，會追蹤具有相容性區段的應用程式。
-   Windows Vista (預設) ：在某些特定情況下無法正確安裝或在執行時間損毀的應用程式會讓 PCA 受到緩和。 如需詳細資訊，請參閱 Resources 區段。

## <a name="leveraging-feature-capabilities"></a>運用功能功能

使用作業系統支援的最新相容性資訊來更新應用程式資訊清單。 本節描述資訊清單的新增專案：

**命名空間：** 相容性。 v1 (xmlns = "urn：架構-microsoft-com：相容性 v1" >) 

**區段名稱：** (新區段的相容性) 

**SupportedOS：** 支援的作業系統 GUID-對應至受支援作業系統的 Guid 如下：

-   {e2011457-1546-43c5-a5fe-008deee3d3f0}

    針對 **Windows Vista**：這是 switchback 內容的預設值

-   {35138b9a-5d96-4fbd-8e2d-a2440225f93a}

    針對 **Windows 7**：在應用程式資訊清單中設定此值的應用程式會取得 Windows 7 行為

-   {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}

    針對 **Windows 8**：在應用程式資訊清單中設定此值的應用程式會取得 Windows 8 行為

Microsoft 會視需要產生並張貼未來 Windows 版本的 Guid。

已更新之資訊清單的 XML 範例：

> [!Note]  
> 應用程式資訊清單中的屬性和標記名稱會區分大小寫。

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



上述範例中所有作業系統的 Guid 都提供下層支援。 支援多個平臺的應用程式不需要每個平臺都有不同的資訊清單。

## <a name="tests"></a>測試

應用程式可以指定多個支援的作業系統識別碼。 如果您已在該作業系統上測試或正在測試應用程式，則應該新增支援的作業系統識別碼。 Windows Vista 和先前的作業系統版本不會注意這些專案。 從 Windows 7 開始，Windows 會在資訊清單中選擇最高版本的 GUID，直到執行中的 Windows 版本，並提供該層級的應用程式支援。 若要使用新的應用程式資訊清單相容性區段確認應用程式是否正常運作：

1.  使用新的相容性區段和 SupportedOS ID = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} 測試應用程式，以確保應用程式能夠使用最新的 Windows 8 行為來正常運作。
2.  使用新的相容性區段和 SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} 測試應用程式，以確保應用程式能夠使用 Windows 7 行為正常運作。
3.  使用新的相容性區段和 SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0} 測試應用程式，以確保應用程式能夠使用 Windows Vista 行為正常運作。

## <a name="resources"></a>資源

-   [QueryActCtxW 函式](../sbscs/application-manifests.md)
-   [UAC 資訊清單](/previous-versions/bb756929(v=msdn.10))
-   [Windows 應用程式的應用程式資訊清單](../sbscs/application-manifests.md)
-   [桌面視窗管理員 (DWM) ](../dwm/dwm-overview.md)
-   [內容不相符更新](https://support.microsoft.com/kb/978637)
-   [程式相容性助理](/previous-versions/bb756937(v=msdn.10))

 

 