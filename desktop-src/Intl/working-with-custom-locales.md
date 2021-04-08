---
description: 本主題提供一些指示，說明如何處理應用程式中的自訂地區設定。
ms.assetid: 2622e2b3-b952-4666-a440-85d73d11c5e0
title: 使用自訂地區設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0e59446496ae2985860c0fd6b1bd5bddde084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943718"
---
# <a name="working-with-custom-locales"></a>使用自訂地區設定

本主題提供一些指示，說明如何處理應用程式中的 [自訂地區](custom-locales.md) 設定。 因為您的應用程式不會控制作業系統上是否已安裝自訂地區設定，所以最好以這些考慮來準備所有的原始程式碼。

## <a name="handle-locale_stime-constant-correctly"></a>正確處理地區設定 \_ STIME 常數

如果您的繼承應用程式使用 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 取得 [地區設定 \_ STIME](locale-stime-constants.md)所指出的過時時間分隔符號，則應用程式可能無法剖析時間格式。 請記住，以分鐘為單位分隔小時的字元與從秒分隔分鐘的字元不同。

> [!Note]  
> 當您針對自訂地區設定進行程式設計時，請記住它們不尋常。 所有適用于 NLS 的欄位幾乎都必須處理不尋常的行為。 例如，時間格式 12H34 ' 12 ' ' 是合法的，而且通常是可理解的。 但許多應用程式也會對可能會中斷緩衝區長度或顯示欄位的時間分隔符號提出假設。

 

## <a name="distinguish-among-supplemental-locales"></a>區分補充地區設定

所有補充地區設定都使用地區設定[識別碼](locale-identifiers.md)的[地區設定 \_ 自訂 \_ 未指定](locale-custom-constants.md)常數。 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)無法區別補充的地區設定，但 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)可能是因為它使用地區設定 [名稱](locale-names.md)，而非地區設定識別碼。 只有當該地區設定是目前選取的使用者地區設定時，您的應用程式才能取得特定補充地區設定的相關資訊。 然後，應用程式可以呼叫 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 並傳遞常數 [地區設定 \_ 使用者 \_ 預設值](locale-user-default.md) 作為地區設定識別碼。

## <a name="handle-replacement-locales"></a>處理取代地區設定

若要保留 Windows 的可靠性，請記住，您的應用程式所支援的取代地區設定無法修改取代地區設定的地區設定識別碼。 取代地區設定都不能修改 Windows 的排序屬性。

雖然取代地區設定可以變更預設行事曆，但它必須將原始預設值保留在可用行事曆清單中的某個位置。 例如，泰文 (泰國) 地區設定會使用泰文曆日曆作為預設值。 系統管理員可以建立使用西曆當地語系化日曆的取代地區設定。 不過，可用的行事曆清單會繼續包含泰國曆日曆的專案。

針對取代地區設定，您的應用程式通常應該查閱地區設定特定資訊，而不是根據特定地區設定的知識來嘗試「快捷方式」。 例如，當 [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) 將目前的地區設定視為英文 (美國) 時，實際上可能是應允許生效的取代地區設定。

## <a name="customize-calendars"></a>自訂行事曆

您的應用程式可以針對西曆自訂日期和月份名稱，但不能針對非西曆行事曆。 同樣地，NLS 不支援建立使用者定義的自訂行事曆。 如需詳細資訊，請參閱 [日期和行事曆](date-and-calendar.md)。

## <a name="handle-sorting-sequences"></a>處理排序次序

補充地區設定可以使用任何 Microsoft 定義的排序次序。 取代地區設定必須使用與其所取代之地區設定相同的排序次序。 NLS 不支援建立使用者定義的排序次序。 如需詳細資訊，請參閱 [在您的應用程式中處理排序](handling-sorting-in-your-applications.md)。

## <a name="localize-custom-locale-information"></a>將自訂地區設定資訊當地語系化

NLS 不提供當地語系化自訂地區設定資訊的機制。 因此，用來做為自訂地區設定之地區設定識別碼的常數 [地區設定 \_ SLANGUAGE](locale-slanguage.md) 或 [地區設定 \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md) 一律會抓取與 [地區設定 \_ SNATIVELANGNAME](locale-snative-constants.md) 或 [地區設定 \_ SNATIVELANGUAGENAME](locale-snative-constants.md)相關聯的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用國家語言支援](using-national-language-support.md)
</dt> <dt>

[自訂地區設定](custom-locales.md)
</dt> <dt>

[日期和行事曆](date-and-calendar.md)
</dt> <dt>

[處理應用程式中的排序](handling-sorting-in-your-applications.md)
</dt> </dl>

 

 



