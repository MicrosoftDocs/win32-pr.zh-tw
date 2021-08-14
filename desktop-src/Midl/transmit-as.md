---
title: transmit_as 屬性
description: '\ 傳輸 \_ as \ 屬性會指示編譯器將型別識別碼（用戶端和伺服器應用程式操作的呈現型別）與傳送的型別 xmit 類型產生關聯。'
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- transmit_as 屬性 MIDL
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d1b8e9aae9a147c929fade8030babbf6b02fd87c9170370252522001742e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382828"
---
# <a name="transmit_as-attribute"></a>傳輸 \_ 為屬性

[ **\[ 傳輸 \_ 為 \]** ] 屬性會指示編譯器將 **型別識別碼**_（_ 用戶端和伺服器應用程式操作的呈現型別）與傳輸類型 **xmit 類型** 產生關聯。

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a>參數

<dl> <dt>

*xmit-類型* 
</dt> <dd>

指定在用戶端與伺服器之間傳輸的資料類型。

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

指定套用至類型的一或多個屬性。 有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**字串**](string.md) **\]** 並 **\[** [**忽略**](ignore.md) **\]** 。 以逗號分隔多個屬性。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 [基底類型](midl-base-types.md)、[**結構**](struct.md)、[**等位、**](union.md)[**列舉**](enum.md)類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*宣告子清單* 
</dt> <dd>

指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。 如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。 宣告子 *清單* 包含一或多個以逗號分隔的宣告子。 函式宣告子中的參數宣告子（例如參數名稱）是選擇性的。

</dd> <dt>

*類型識別碼* 
</dt> <dd>

指定呈現給用戶端和伺服器應用程式的資料類型名稱。

</dd> </dl>

## <a name="remarks"></a>備註

若要使用 **\[ 傳輸 \_ 為 \]** 屬性，使用者必須提供在所呈現的和傳輸的類型之間轉換資料的常式; 這些常式也必須釋放用來保存轉換資料的記憶體。 [ **\[ 傳輸 \_ 為 \]** ] 屬性會指示存根呼叫使用者提供的轉換常式。

傳送的型別 *xmit 類型* 必須解析為 MIDL 基底類型、預先定義的類型或類型識別碼。 如需詳細資訊，請參閱 [MIDL 基底類型](midl-base-types.md)。

使用者必須提供下列常式。



| 常式名稱              | Description                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *類型識別碼 * * * \_ 至 \_ xmit**   | 將資料從呈現的型別轉換成傳送的型別。 這個常式會為傳送的型別和傳送的型別中的指標所參考的任何資料，配置記憶體。                            |
| *\_xmit 中的類型識別碼 * * \_** | 將資料從傳送的型別轉換成呈現的型別。 此常式負責針對呈現類型中的指標所參考的資料，配置記憶體。 RPC 會為類型本身配置記憶體。 |
| *類型識別碼 * * * \_ 免費 \_ inst** | 釋出配置給所呈現型別中指標所參考之資料的記憶體。 RPC 會釋出類型本身的記憶體。                                                                                               |
| *類型識別碼 * * * \_ 免費 \_ xmit** | 釋放呼叫端用來傳送的儲存體，以及傳送型別中指標所參考的資料。                                                                                            |



 

 

用戶端 stub 會呼叫 *\_ \_ xmit * 的型別 id * *** 來為傳輸的型別配置空間，以及將資料轉譯成 xmit 類型的物件 *。* 伺服器 stub 會為原始資料類型配置空間，並 *\_ 從 \_ xmit * 呼叫類型識別碼 * * **，以將資料從其傳送的類型轉譯為呈現的型別。

從應用程式程式碼傳回時，伺服器 stub 會呼叫 *類型識別碼 * * * \_ free \_ inst**，以在伺服器端解除配置 *型別識別碼* 的儲存體。 用戶端 stub 會呼叫 *類型 id * * * \_ free \_ xmit**，以在用戶端上解除配置 *xmit 類型* 的儲存體。

下列類型不能有 **\[ 傳輸 \_ 為 \]** 屬性：

-   內容會以 **\[** [**內容 \_ 處理**](context-handle.md)程式類型屬性和型別來處理 (型別 **\]** ，而這些型別是用來當做具有 **\[ 內容 \_ 控制碼 \]** 屬性的參數) 
-   管道或衍生自管道的類型
-   當做管道定義之基底類型使用的資料類型
-   指標或解析為指標的參數
-   符合一致性、變化或開放陣列的參數
-   包含符合標準陣列的結構
-   預先定義的類型 [**控制碼 \_ t**](handle-t.md)、 [**void**](void.md)

傳送的類型必須符合下列限制：

-   它們不得為指標或包含指標。
-   它們不得為管道或包含管道。

## <a name="examples"></a>範例

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[**枚舉**](enum.md)
</dt> <dt>

[**處理**](handle.md)
</dt> <dt>

[**處理 \_ t**](handle-t.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**忽略**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**結構**](struct.md)
</dt> <dt>

[**切換 \_ 類型**](switch-type.md)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[**聯盟**](union.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 