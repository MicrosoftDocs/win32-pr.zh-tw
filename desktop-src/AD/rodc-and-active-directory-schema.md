---
title: Read-Only Dc 和 Active Directory 架構
description: Windows Server 2008 引進了一種新類型的網域控制站， (RODC) 的唯讀網域控制站。
ms.assetid: 9d9082d2-6f7f-4ffa-b8c7-6414be764d0c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4284ffdda7ed2fbe481c201f7da69371209ce55
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104093455"
---
# <a name="read-only-dcs-and-the-active-directory-schema"></a>Read-Only Dc 和 Active Directory 架構

Windows Server 2008 引進了一種新類型的網域控制站， (RODC) 的唯讀網域控制站。 這會提供網域控制站，以便在無法放置完整網域控制站的分公司中使用。 其目的是讓分公司的使用者登入，並執行諸如檔案/印表機共用的工作，即使沒有中樞網站的網路連線。

RODC 不會變更架構的使用方式。 不過，值得一提的是，架構支援 Read-Only 部分屬性集 (RO-PAS) ，也稱為 RODC 已篩選屬性集，這是基於安全性考慮而不會複寫至 Rodc 的特殊屬性集。 RO-PAS 會透過 [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) 屬性在架構中定義。

## <a name="rodc-filtered-attribute-set"></a>RODC 已篩選屬性集

某些使用 [Active Directory Domain Services](active-directory-domain-services.md) 作為資料存放區的應用程式可能會有類似認證的資料 (例如密碼、認證或加密金鑰) 不應儲存在 Read-Only 網域控制站上的應用程式，以免 RODC 遭竊或遭到盜用。 對於這種類型的應用程式，您可以將屬性新增至 RODC 已篩選屬性集，以防止它複寫至樹系中的 Rodc，並將該屬性標示為機密，以移除讀取已驗證使用者群組成員之資料的能力 (包括任何 Rodc) 。

## <a name="adding-attributes-to-the-rodc-filtered-attribute-set"></a>新增屬性至 RODC 已篩選屬性集

RODC 已篩選屬性集為動態屬性集，不會複寫至樹系中的任何 RODC。 您可以在執行 Windows Server 2008 的架構主機上設定 RODC 已篩選屬性集。 當禁止將屬性複寫至 RODC 時，若 RODC 遭竊或被盜用，就可避免資料不慎外洩。

您無法將重要的系統屬性新增至 RODC 已篩選屬性集中。 AD DS、本機安全性授權單位 (LSA)、安全性帳戶管理員 (SAM)，以及任何 Microsoft 特定的安全性服務提供者 (例如，Kerberos 驗證通訊協定) 正常運作所需的屬性，即是重要系統屬性。 在 Beta 3 之後的 Windows Server 2008 版本中，系統關鍵屬性具有 (schemaFlagsEx 屬性值的 schemaFlagsEx 屬性值 & 0x1 = **TRUE**) 。

如需將屬性新增至 RODC 已篩選屬性集的逐步指示，請參閱 [rodc 逐步指南的附錄 D]( /previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772331(v=ws.10))。

## <a name="marking-attributes-as-confidential"></a>將屬性標示為機密

此外，設定為 RODC 已篩選屬性集之一部分的任何屬性，建議您也將其標示為機密。 若要將屬性標示為機密，必須移除 Authenticated Users 群組對於該屬性的讀取權限。 將屬性標示為機密，可移除讀取類似認證的資料所需的權限。當 RODC 被盜用時，可提供額外的保護。 如需將屬性標示為機密的詳細資訊，請參閱 [Microsoft 知識庫中的文章 922836]( https://support.microsoft.com/kb/922836)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[唯讀網域控制站逐步指南]( https://support.microsoft.com/kb/922836)
</dt> </dl>

 

 