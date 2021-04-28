---
description: 移除 Windows Mail
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: 移除 Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50ad1008d9e252e1705a159f19d362677934023
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116276"
---
# <a name="removal-of-windows-mail"></a>移除 Windows Mail

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-Windows 7  
**伺服器** -Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

**嚴重性** -高  
**頻率** -高  









## <a name="description"></a>Description

Microsoft 正在淘汰 Windows Mail 公用程式，並停用 API CoStartOutlookExpress。 其他郵件 Api 已標示為已淘汰，並預定在稍後的 Windows 版本中移除。 不過，未標示為已淘汰或已淘汰的公開記錄 Api 將會在 Windows 7 中繼續運作。 二進位檔會保留在使用者的系統上，而且會繼續透過 Api 存取，尤其是在上述情況下。 此外，使用者的電子郵件 ( .eml) 和新聞 ( nws) 檔會保留在系統上。

## <a name="manifestation-of-impact"></a>影響的表現

移除 Windows Mail 會導致下列情況：

-   所有進入 Windows Mail 和 Contacts 的進入點都 (例如，[開始] 功能表、使用者建立的快捷方式、[開始 > 執行]，) 移除或停用。 其中有些會完全移除，而其他則會在嘗試啟動時失敗。
-   所有 Dll 都隨附于 box
-   公開記載的 Api 仍會像在 Windows Vista 中一樣繼續運作。
-   任何嘗試啟動主要瀏覽器 UI 的 Api 都已經過修改，以建立無訊息失敗。 函數會傳回成功，但不會向使用者顯示 UI。 呼叫其他對話方塊的 Api (例如，[多工緩衝處理器] 或 [帳戶] 對話方塊，) 繼續顯示該 UI
-   通訊協定 (mailto、ldap、news、snews、nntp) 處理常式將不會與 Windows Mail 或 Contacts 相關聯。 當您嘗試啟動這些專案時，客戶會看到錯誤對話方塊，指向可將這些關聯設定到其他程式的位置。
-   檔案關聯 ( .eml、nws、. contact、. group、.wab、. p7c、. vfc) 已中斷或停用。 當嘗試使用這些延伸模組開啟檔案時，客戶會看到一個對話方塊，提供他們可使用的其他應用程式，並將其指向提供解決方案的網頁
-   任何使用者檔案 (例如，連絡人檔案或訊息) 在升級案例中會保留在系統上
-   [連絡人] 資料夾預設為隱藏，因此客戶不會看到它
-   Api 在 MSDN 中標示為已淘汰
-   檔案預覽功能已移除
-   滑鼠右鍵功能表中的 Shell 勾點已移除
-   檔案搜尋功能已移除

## <a name="mitigation"></a>降低

使用者應該安裝 Windows Live Mail 或任何其他能夠讀取 .eml 和. nws 檔案的郵件產品。

## <a name="solution"></a>解決方法

偵測是否已安裝預設郵件處理常式。 如果沒有，請通知使用者安裝 Windows Live Mail 或任何能夠讀取 .eml 和. nws 檔案的其他產品。

請勿設計呼叫 Windows Mail UI API 的程式碼，因為它將無法運作。 您必須找到其他存取 .eml 和. nws 檔案的方式。 此外，只要可行，就不再依賴所有其他 Windows Mail Api。

## <a name="compatibility-performance-reliability-and-usability-testing"></a>相容性、效能、可靠性和可用性測試

-   在 Windows 7 環境中練習您的應用程式，以確保應用程式不會嘗試呼叫 UI API。
-   或者，您也可以使用 Windows 相容性評估工具 (ACT) 來執行應用程式相容性工具組 (WCE) ，以找出這項功能的取代可能發生的任何問題。

## <a name="links-to-other-resources"></a>其他資源的連結

<dl>

[應用程式相容性工具組下載](/windows-hardware/get-started/adk-install)  
</dl>

 

 
