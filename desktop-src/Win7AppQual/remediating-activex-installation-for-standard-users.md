---
description: 修正標準使用者的 ActiveX 安裝相容性問題
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: 修正標準使用者的 ActiveX 安裝相容性問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31dbcf8dfddd7e35a8a446f4b73dd1e5324cbe4695590511fa1cb220700b2c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994768"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a>修正標準使用者的 ActiveX 安裝相容性問題

若要開發安全的桌面環境，您必須減輕惡意 ActiveX 控制項的威脅，並在您的環境中提供適當層級的應用程式相容性。 *ActiveX 控制項* 是可執行程式碼的一部分 (通常是封裝在封包檔中的 OCX 檔案，) 是透過 Windows Internet Explorer 安裝和執行。 您可以建立 ActiveX 控制項，將功能新增至 web 應用程式，您無法使用標準的 HTML 程式碼或簡單的腳本輕鬆達成。

當您遷移至 Windows 7 時，安裝 ActiveX 控制項會成為相容性的問題，包括轉換至標準使用者。 這種類型的轉換是 IT 專業人員將其環境移至 [標準使用者帳戶](https://support.microsoft.com/hub/4338813/windows-help)的一般最佳作法。 這項轉換不需要部署 Windows Internet Explorer 8。

## <a name="activex-control-installation"></a>ActiveX控制安裝

ActiveX 控制項都有一個簡單的下載和執行部署模型。 ActiveX 控制項是透過 HTML **物件** 元素安裝和執行。 此專案的程式 **代碼基** 底屬性會使用 URL 來指示 Internet Explorer () 如果使用者的電腦上尚未安裝該控制項，則會在該位置取得控制項。 在這種情況下，Internet Explorer 會下載相關聯的安裝套件、在物件上執行信任驗證，並在 Internet Explorer 提示使用者提供安裝許可權。

在安裝期間，轉譯頁面會註冊並執行控制項。 在安裝控制項之後，任何標準使用者都可以執行控制項。 這種簡單的散發和執行機制提供簡單的方法，將您的元件散發給 web 應用程式的使用者。 但是標準帳戶使用者無法直接安裝每部電腦的 ActiveX 控制項，而且可能需要系統管理員許可權才能完成安裝。

## <a name="activex-installer-service-axis"></a>ActiveX安裝程式服務 (軸) 

ActiveX 安裝程式服務 (軸) 可讓您在組織中的電腦上使用群組原則部署 ActiveX 控制項。 您可以群組原則設定來設定軸，您可以使用群組原則管理主控台 (GPMC) 或本機群組原則編輯器來修改這些設定。

有兩個適用于軸的原則設定：

-   [ActiveX 控制項的核准安裝網站] 原則設定是由已核准的安裝網站清單所組成，此清單可讓軸用來判斷是否可以安裝 ActiveX 控制項。
-   [信任的區域中的網站的 ActiveX 安裝原則] 原則設定會識別信任的網站區域如何用來安裝 ActiveX 控制項。

當網站嘗試安裝 ActiveX 控制項時，該軸會檢查網站的 URL 是否列在已核准的安裝網站清單中，或作為 [信任的網站] 區域的一部分。 如果網站是在其中一個清單中，則軸會確定該網站符合原則所定義的需求。 如果網站和 ActiveX 控制項符合原則設定的所有需求，就會安裝該控制項。 如需詳細資訊，請參閱[管理 ActiveX 安裝程式服務](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10))。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用相容性檢視修正 Web 應用程式中的相容性問題](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
