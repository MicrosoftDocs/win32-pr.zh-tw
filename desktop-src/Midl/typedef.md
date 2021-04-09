---
title: typedef 屬性
description: IDL typedef 關鍵字允許與 C 語言 typedef 宣告非常類似的 typedef 宣告。
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- typedef 屬性 MIDL
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681818"
---
# <a name="typedef-attribute"></a>typedef 屬性

IDL **typedef** 關鍵字允許與 C 語言 **typedef** 宣告非常類似的 **typedef** 宣告。

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a>參數

<dl> <dt>

*idl-類型-屬性清單* 
</dt> <dd>

指定套用至類型的一或多個屬性。 IDL 檔案中的有效類型屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md) **\]** ; 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 、 **\[** [**字串**](string.md)和 **\]** **\[** [**忽略**](ignore.md) **\]** 。 以逗號分隔多個屬性。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 [基底類型](midl-base-types.md)、[**結構**](struct.md)、[**等位、**](union.md)[**列舉**](enum.md)類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。 [**Const**](const.md)關鍵字可以在 *類型規範* 之前。

</dd> <dt>

*宣告子清單* 
</dt> <dd>

指定標準 MIDL 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。 如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。 宣告子清單包含一或多個宣告子， *並* 以逗號分隔。

</dd> <dt>

*acf-type-attribute-list* 
</dt> <dd>

指定套用至類型的一或多個屬性。 ACF 中的有效類型屬性包括 **\[** [**配置**](allocate.md) **\]** 、 **\[** [**編碼**](encode.md) **\]** 和解碼 **\[** [](decode.md) **\]** 。

</dd> <dt>

*typename* 
</dt> <dd>

指定 IDL 檔案中定義的類型。

</dd> </dl>

## <a name="remarks"></a>備註

IDL **typedef** 宣告已增強，可讓您將類型屬性與定義的類型產生關聯。 有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md) **\]** ; 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 、 **\[** [**字串**](string.md) **\]** 和 **\[** [**略**](ignore.md)過 **\]** 。

ACF 中的 **typedef** 關鍵字會將屬性套用至對應 IDL 檔案中所定義的類型。 例如，[ [**配置**](allocate.md) 類型] 屬性可讓您自訂應用程式和存根的記憶體配置和解除配置。

ACF **typedef** 語句會顯示為 ACF 主體的一部分。 請注意，ACF **typedef** 語法與 IDL **Typedef** 語法和 C 語言 **typedef** 語法不同。 ACF 中不會引進任何新的類型。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**分配**](allocate.md)
</dt> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[**解碼**](decode.md)
</dt> <dt>

[**編碼**](encode.md)
</dt> <dt>

[**枚舉**](enum.md)
</dt> <dt>

[**處理**](handle.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**忽略**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**字串**](string.md)
</dt> <dt>

[**結構**](struct.md)
</dt> <dt>

[**切換 \_ 類型**](switch-type.md)
</dt> <dt>

[**傳輸 \_ 為**](transmit-as.md)
</dt> <dt>

[**聯盟**](union.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> </dl>

 

 