---
title: 備份與還原 DRM 授權
description: 備份與還原 DRM 授權
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Windows Media Format SDK，備份 DRM 授權
- Windows Media Format SDK，還原 DRM 授權
- Windows Media Format SDK，DRM 授權
- Windows Media Format SDK，DRM 的授權
- Windows Media Format SDK，備份還原功能
- Windows Media Format SDK，授權管理服務
- Windows Media Format SDK，詐騙偵測
- 數位版權管理 (DRM) ，備份授權
- DRM (數位版權管理) ，備份授權
- 數位版權管理 (DRM) ，還原授權
- DRM (數位版權管理) ，還原授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) ，備份還原功能
- DRM (數位版權管理) ，備份還原功能
- 數位版權管理 (DRM) ，授權管理服務
- DRM (數位版權管理) ，授權管理服務
- 數位版權管理 (DRM) ，詐騙偵測
- DRM (數位版權管理) ，詐騙偵測
- 備份 DRM 授權
- 還原 DRM 授權
- 授權，DRM
- 授權，備份 DRM
- 授權，還原 DRM
- 備份還原功能
- 授權管理服務
- 詐騙偵測
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7718f03170077f7db624f8a99b8262239a79ca9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104316651"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a>備份與還原 DRM 授權

使用備份還原功能時，使用者可以將 [*授權*](wmformat-glossary.md) 備份和還原到同一部電腦或其他電腦。 這項功能可讓使用者在重新格式化硬碟之後，將授權傳送到新的電腦或回到同一部電腦 (，例如) 。 此外，使用者也可以在一部以上的電腦上播放受保護的 ASF 檔案。

為了鼓勵合法使用授權，詐騙偵測原則會限制可以還原授權的次數。 Microsoft 提供的服務會追蹤已還原授權的電腦數目;如果達到限制，則使用者無法還原授權。

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a>允許或不允許備份和還原的許可權

備份還原功能只適用于提供備份和還原許可權的授權。 如果內容擁有者或授權簽發者不想要這項功能，或它們發出的授權包含安全狀態 (例如計數作業或有限的時間) ，則可以不允許這種許可權。

當授權無法還原，因為使用者沒有許可權，就會將 [*金鑰識別碼*](wmformat-glossary.md) 傳遞至應用程式。 使用者至少應該收到某些授權無法備份的通知，但使用者不知道此訊息所參考的授權。 如果您知道可用受保護檔案的金鑰識別碼，您可以開發更健全的解決方案來通知使用者。

例如，您可以針對在網際網路上提供受保護的歌曲的記錄標籤開發播放機。 這些歌曲及其金鑰識別碼可在資料庫中追蹤。 如果某些授權無法備份，播放程式應用程式可以使用金鑰識別碼來查詢資料庫中的歌曲名稱，然後通知使用者無法備份授權的歌曲。 或者，您可以在本機為每位使用者建立音樂媒體櫃，而且金鑰識別碼可以用來取得有關哪些授權無法備份的詳細資訊。

## <a name="the-license-management-service"></a>授權管理服務

當執行備份還原功能時，由 Microsoft 託管的授權管理服務會管理授權的還原。

首先，使用者會在應用程式中備份授權，例如選擇功能表選項。 電腦上的所有授權都會備份到指定的位置，例如磁片磁碟機。 然後，使用者會使用應用程式來還原授權，例如，選擇功能表選項並指定其備份位置。

此時，使用者必須連線到網際網路。來自應用程式的要求會傳送至授權管理服務。 如果備份授權的電腦與原始電腦不同 (或原始電腦已) 重新格式化，則授權管理服務會對新電腦發出新的授權。 否則，就會重新發出先前發行給該電腦的授權。

因為授權管理服務會抓取使用者的資訊，所以您必須在 [Microsoft 網站](https://www.microsoft.com/licensing/default)上顯示 microsoft 隱私權原則或提供該頁面的連結。

> [!Note]  
> 當使用者將授權還原至不同的電腦，而且授權需要使用個人化時，終端使用者必須授權 DRM 元件更新。 您必須在播放程式應用程式中執行程式，以支援這項功能。

 

## <a name="detecting-fraud"></a>偵測詐騙

允許使用者將授權還原為有限的次數。 每次還原授權時，授權管理服務都會追蹤它，並將該授權的計數遞增一。 將授權還原至先前已還原授權的電腦時 (例如，用來備份授權的電腦) ，則不會增加計數。 如果電腦有新的作業系統，或已重新安裝作業系統，則會被視為不同的電腦。

根據 Microsoft 的詐騙偵測原則，當授權經過一定次數的還原時，應用程式會接收來自 DRM 元件的 URL，並負責開啟瀏覽器並顯示網頁，指出可能違反授權合約。 使用者必須與授權散發者聯繫，之後必須判斷要求是否有效。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**數位 Rights Management 功能**](digital-rights-management-features.md)
</dt> <dt>

[**備份和還原授權**](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




