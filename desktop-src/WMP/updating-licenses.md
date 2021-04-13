---
title: 更新授權
description: 更新授權
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Windows Media Player 線上商店，更新授權
- 線上商店，更新授權
- 輸入1個線上商店，更新授權
- Windows Media Player 線上商店、授權更新
- 線上商店、授權更新
- 輸入1個線上商店、授權更新
- 更新授權
- 授權，更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154959b01c93719184e310b60dffaa91fe2dcfa0
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314274"
---
# <a name="updating-licenses"></a>更新授權

線上商店可以傳遞經過特定一段時間或特定日期的授權內容。 這在訂用帳戶服務合約中提供的音樂內容是正常的。 在此情況下，線上商店必須有機會在這些授權到期之前更新這些授權（當然，假設使用者已付費續訂其訂用帳戶。  (如果使用者尚未更新訂用帳戶，則只會讓授權保持過期。 ) 

Windows Media Player 會查詢內容合作夥伴外掛程式有關播放程式應針對即將到期的授權提供多少預先警告的警告。 它會藉由呼叫 [IWMPContentPartner：： GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo)，並 \_ \_ 透過 *bstrInfoName* 參數傳遞常數 g szContentPartnerInfo LicenseRefreshAdvanceWarning 來執行此動作。 若要針對即將到期的授權警示外掛程式，Windows Media Player 呼叫 [IWMPContentPartner：： RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense)。 此呼叫會取得參數，以提供正在重新整理之檔案的詳細資料，例如檔案是否在使用者的電腦上，以及檔案的路徑。 如果在裝置同步處理作業中重新整理授權， *pReasonCoNtext* 參數會提供裝置的 cannonical 名稱。

當 Windows Media Player 呼叫 **RefreshLicence** 時，它會傳遞可識別更新要求的 cookie。 當外掛程式完成處理更新要求時，它會呼叫 [IWMPContentPartnerCallback：： RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete)來通知 Windows Media Player，傳遞 cookie、媒體專案的識別碼，以及表示更新是否成功的 **HRESULT** 。

線上商店外掛程式也可以在背景進程中進行授權檢查和更新。 Windows Media Player 藉由呼叫 [IWMPContentPartner：： Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify)，通知外掛程式有關允許執行背景處理工作的時間。 為了指示外掛程式啟動背景處理，播放 [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) 列舉值 wmpsnBackgroundProcessingBegin;為了指示外掛程式停止背景處理，播放 wmpsnBackgroundProcessingEnd 會傳遞值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型1線上商店的程式設計指南**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




