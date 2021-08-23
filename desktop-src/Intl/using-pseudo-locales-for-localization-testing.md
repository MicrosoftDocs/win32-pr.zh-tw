---
description: 在 Windows Vista 和更新版本上，您可以使用虛擬地區設定來測試應用程式的可當地語系化性。 本主題包含使用虛擬程式碼的程式。
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: 使用虛擬地區設定進行當地語系化測試
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: 72d84cbf324823a814c9412580b033792b0d1c8a45630bf2f4cb26dd8b2a1acf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631718"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a>使用虛擬地區設定進行當地語系化測試

[虛擬地區設定](pseudo-locales.md)內建于 Windows Vista 和更新版本，因此您可以透過 (NLS) api 的國家語言支援來存取它們。 您可以使用虛擬地區設定來測試應用程式的可 [當地語系化](/windows/uwp/design/globalizing/globalizing-portal) 性。 本主題包含使用虛擬程式碼的程式。

> [!NOTE]
> 在虛擬地區設定中，需要特別考慮的一項工作就是列舉它們;不論是在您的程式碼中，或是在主控台的地區和語言選項部分中。 本主題稍後將詳細說明。

虛擬地區設定的名稱為 "qps-qps-ploc"、"qps-ploca" 和 "qps-plocm"。 從 Windows 10，虛擬地區設定 "qps-Latn-x-sh" 也可供使用。

## <a name="retrieve-information-about-pseudo-locales"></a>取得虛擬地區設定的相關資訊

您可以使用 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 來取得虛擬地區設定的相關資訊。 將特定虛擬地區設定的名稱傳遞至函式 (查看上述) 的名稱清單。 例如，針對鏡像虛擬地區設定的 "qps-plocm"。

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a>搭配使用 LocaleNameToLCID 與虛擬地區設定

您可以使用虛擬地區設定的名稱來呼叫 NLS 對應函式 [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) 。

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a>啟用列舉的虛擬地區設定

在您的應用程式中，您可以呼叫 [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) 來列舉系統識別的地區設定。 主控台的 [地區及語言選項] 部分也會呼叫 **EnumSystemLocalesEx** 來建立所顯示的地區設定清單。 不過，根據預設，系統不會辨識上面所列的四個虛擬地區設定，因此 **EnumSystemLocalesEx** 不會傳回它們。 針對 Windows Vista （含）以上的系統（包括 Windows 10 1709 版），解決方案是藉由將金鑰新增至 Windows 登錄來啟用虛擬地區設定。

您可以在 HKEY \_ LOCAL \_ MACHINE \\ system \\ CurrentControlSet \\ Control \\ Nls 金鑰下，針對作業系統上安裝的語言來進行編輯。 您可以進行這些設定，以啟用虛擬地區設定。 以下顯示的每個金鑰都是對應至所要啟用虛擬地區設定的十六進位 LCID。 每個值都是字串類型， (REG \_ SZ) 。

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

針對 Windows 10 1803 版，像這樣編輯 Windows 登錄沒有任何作用。 但是您仍然可以使用虛擬地區設定的名稱來呼叫非列舉 NLS Api (請參閱上述的程式碼範例) ，以 (UI) 填入您的使用者介面。

## <a name="related-topics"></a>相關主題

* [使用國家語言支援](using-national-language-support.md)
* [虛擬地區設定](pseudo-locales.md)
* [EnumSystemLocalesEx](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [GetLocaleInfoEx](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [LocaleNameToLCID](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
