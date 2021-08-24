---
description: 地區設定名稱是根據 RFC 4646 (Windows Vista 和更新版本) 的語言標記慣例，並以地區設定 SNAME 來表示 \_ 。
ms.assetid: 221aae7b-3a7c-4995-ae78-50d97de436d8
title: 地區設定名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed4c09900544e96c0f05166d1f4054972e9d8ff89fc108c185695a7506859bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147400"
---
# <a name="locale-names"></a>地區設定名稱

[地區](locales-and-languages.md)設定名稱是根據 RFC 4646 (Windows Vista 和更新版本) 的語言標記慣例，並以[地區設定 \_ SNAME](locale-sname.md)來表示。 一般而言， `<language>-<REGION>` 會使用此模式。 在這裡，language 是小寫的 ISO 639 語言代碼。 如果有的話，會使用 ISO 639-1 中的代碼。 否則，會使用 ISO 639-2/T 中的代碼。 區域指定大寫的 ISO 3166-1 國家/地區識別碼。 例如，英文 (美式的地區設定名稱) 為 "en-us"，而迪維 () 馬爾地夫的地區設定名稱是 "dv-MV"。

> [!Note]  
> 固定的 [地區設定 \_ 名稱 \_ 最大 \_ 長度](locale-name-constants.md) 會提供地區設定名稱的最大長度。 它包含結束的 null 字元的空間。

 

如果地區設定是中性地區設定 (沒有任何區域) ，地區設定 [ \_ SNAME](locale-sname.md) 值會遵循此模式 `<language>` 。 如果這是腳本很重要的中性地區設定，則模式為 `<language>-<Script>` 。

如果您必須使用不同的腳本，從相同語言和區域的另一個地區設定來區分地區設定，則地區設定 \_ SNAME 值會遵循此模式 `<language>-<Script>-<REGION>` ，其中腳本是首字母的 [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html) 腳本。 例如， \_ 特定地區設定烏茲別克 (拉丁，烏茲別克) 的地區設定 SNAME 值為 "uz-Latn-uz"。 當語言通常只會在一個腳本中寫入時，不會包含腳本元件。

地區設定的排序次序會使用 [排序次序識別碼](sort-order-identifiers.md)來指定，例如，排序 \_ 預設值。 為了區分相同語言和區域的兩個或多個排序次序，地區設定名稱會遵循此模式 `<language>-<REGION>\_<sort order>` 。 如果您必須區分腳本和排序次序，則名稱會遵循模式 `<language>-<Script>-<REGION>\_<sort order>` 。 預設的排序次序絕對不會明確指定，只會指定替代的排序次序。 例如，匈牙利文 () 匈牙利預設值為 [排序] 預設值， \_ 或指定的數位相等排序 [匈牙利文] \_ \_ 預設值為 [hu-hu]。 使用排序次序排序匈牙利文的匈牙利文 (匈牙利) \_ 匈牙利文 \_ 技術是指定為 "HU-hu \_ technl"。

若為 [取代地區](custom-locales.md)設定，地區設定名稱必須與要取代之地區設定的名稱相同。 針對補充地區設定，地區設定名稱應遵循或的模式 `<language>-<REGION>-x-<custom>` `<language>-<Script>-<REGION>-x-<custom>` ，其中 `<custom>` 是補充地區設定特有的英數位元字串。 例如，稱為 >fabricam.com 的公司專屬的補充地區設定可能稱為「en-us->fabricam.com」。

應用程式可以使用 [**GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) 和 [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename) 函數來取得目前的地區設定名稱。 雖然每個執行緒都可以使用 [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) 來取得和設定本身的地區設定識別碼，並使用 [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)進行設定，但沒有類似的函數可依名稱取得和設定地區設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[地區設定和語言](locales-and-languages.md)
</dt> <dt>

[自訂地區設定](custom-locales.md)
</dt> <dt>

[地區設定識別碼](locale-identifiers.md)
</dt> <dt>

[排序次序識別碼](sort-order-identifiers.md)
</dt> </dl>

 

 



