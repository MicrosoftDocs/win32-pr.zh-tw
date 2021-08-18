---
description: 正在抓取和設定地區設定資訊
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: 正在抓取和設定地區設定資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d02c2bb58328529781309ce8284310acbcb6fb545ecdc076df295cd020344a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130308"
---
# <a name="retrieving-and-setting-locale-information"></a>正在抓取和設定地區設定資訊

應用程式必須能夠取得及設定有關可用 [地區設定和語言](locales-and-languages.md)的特定資訊。 地區設定資訊的每個專案（例如一周的特定一天名稱或作為小數分隔符號的字元）都有對應的常數。 可用的常數會定義于 [地區設定資訊常數](locale-information-constants.md)中。

您的應用程式一律會將地區設定資訊儲存並操作為以 null 結束的字串。 不允許任何二進位資料，而且必須將任何數值指定為文字。 每種類型的資訊都有特定的格式。 此外，也會將數個型別連結在一起，如此一來，變更一種類型也會變更另一種類型的值。

為了抓取地區設定資訊，應用程式會以與所需資訊對應的常數來呼叫 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 或 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 。 應用程式可以呼叫 [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) 來設定地區設定資訊的專案。

> [!Note]  
> 雖然可能會支援 [地區設定識別碼](locale-identifiers.md) ，但它無法供應用程式使用，除非也已安裝對應的地區設定。

 

因為大部分的地區設定資訊常數都是互斥的，所以一次只能處理一種類型的資訊。 這項規則的例外狀況為 [地區設定 \_ 使用 \_ CP \_ ACP](locale-use-cp-acp.md)、地區設定傳回 [ \_ \_ 編號](locale-return-constants.md)和 [地區設定 \_ NOUSEROVERRIDE](locale-nouseroverride.md)，可以使用二進位或來結合其他常數。

> [!Caution]  
> 強烈建議您不要使用地區設定 \_ NOUSEROVERRIDE，因為它會停用使用者喜好設定。

 

如同一些應用程式，例如 Microsoft Active Directory，您的應用程式可以在可排序的資料庫中維護其字串。 如需詳細資訊，請參閱 [在您的應用程式中處理排序](handling-sorting-in-your-applications.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用國家語言支援](using-national-language-support.md)
</dt> <dt>

[地區設定資訊常數](locale-information-constants.md)
</dt> <dt>

[處理應用程式中的排序](handling-sorting-in-your-applications.md)
</dt> <dt>

[使用自訂地區設定](working-with-custom-locales.md)
</dt> </dl>

 

 



