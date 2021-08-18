---
title: represent_as 屬性
description: '\ 代表 \_ as \ ACF 屬性會將目的語言 repr 類型中的命名區欄位型別與在用戶端和伺服器之間傳送的傳輸類型命名為-type 產生關聯。'
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as 屬性 MIDL
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c76576a7d6710c54573ff78186b3cf6d347afc8c4c242fd6e4c1d49865fb521f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146361"
---
# <a name="represent_as-attribute"></a>表示 \_ 為屬性

**\[ 代表 \_ as \]** ACF 屬性會將目的語言 *repr 類型* 中的命名區欄位型別與在用戶端和伺服器之間傳輸的傳輸類型 *命名為類型*。

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a>參數

<dl> <dt>

*命名類型* 
</dt> <dd>

指定在用戶端與伺服器之間傳送的命名傳輸資料類型。

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

指定套用至類型的一或多個屬性。 以逗號分隔多個屬性。

</dd> <dt>

*repr-類型* 
</dt> <dd>

以呈現給用戶端和伺服器應用程式的目的語言指定表示的區欄位型別。

</dd> </dl>

## <a name="remarks"></a>備註

當使用 **\[ 表示 \_ 為 \]** 時，您必須提供在本機與傳輸類型之間轉換的常式，以及用來保存轉換資料的可用記憶體。 **\[ 代表 \_ as \]** 屬性會指示存根呼叫使用者提供的轉換常式。

*已* 傳送的型別必須解析為 MIDL 基底類型、預先定義的類型或類型識別碼。 如需詳細資訊，請參閱 [MIDL 基底類型](midl-base-types.md)。

您必須提供下列常式：



| 常式名稱                   | 描述                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *\_ \_ 來自本機的命名類型 * * * \_** | 將資料從本機類型轉換為網路類型。 常式會配置網路資料類型的記憶體，包括網路資料類型中指標所參考之任何資料的記憶體。              |
| *命名 \_ 類型 * * * \_ 至 \_ 本機**   | 將資料從網路類型轉換成區欄位型別。 常式負責為本機類型中的指標所參考的資料配置記憶體。 RPC 會為本機類型本身配置記憶體。 |
| *命名 \_ 類型 * * * \_ 可用 \_ 本機** | 釋出配置給本機類型之指標所參考之資料的記憶體。 RPC 釋出類型本身的記憶體                                                                                             |
| *命名 \_ 類型 * * * \_ 免費 \_ inst**  | 釋出為網路類型和網路類型本身的指標所參考的資料所配置的記憶體。                                                                                            |



 

用戶端 stub 會 *\_ 從 \_ 本機 * 呼叫名為 type * ***，以配置已傳送類型的空間，以及將資料從本機類型轉譯為網路類型。 伺服器 stub 會配置原始資料類型的空間，並呼叫 *名稱為 * * * 的 \_ \_ 本機**，將資料從網路類型轉譯為本機類型。

從應用程式程式碼傳回時，用戶端和伺服器 stub 會呼叫 *指名型別 * * * \_ free \_ inst** 來解除配置網路類型的儲存體。 用戶端 stub 會呼叫 *名為 type * * * \_ free \_ local** 來解除配置常式所傳回的儲存區。

下列類型不能有 **\[ 代表 \_ 做為 \]** 屬性：

-   一致、變化或一致的陣列
-   結構，其中最後一個成員是一致的陣列 (一致的結構) 
-   包含指標的指標或類型
-   包含管道的管道或類型
-   用來作為管道基底類型的類型
-   預先定義的類型會 [**處理 \_ t**](handle-t.md)、 [**void**](void.md)
-   具有 [**\[ handle \]**](handle.md)屬性的類型

## <a name="examples"></a>範例

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**處理 \_ t**](handle-t.md)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 




