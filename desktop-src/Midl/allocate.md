---
title: 配置屬性
description: '\ 配置 \ ACF 屬性可讓您自訂 IDL 檔案中定義之類型的記憶體配置和解除配置。'
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- 配置屬性 MIDL
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841155"
---
# <a name="allocate-attribute"></a>配置屬性

**\[ 配置 \]** ACF 屬性可讓您自訂 IDL 檔案中定義之類型的記憶體配置和解除配置。

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a>參數

<dl> <dt>

*配置-選項-清單* 
</dt> <dd>

指定一或多個記憶體配置選項。 選取 **單一 \_ 節點** 或 **所有 \_ 節點** 的其中一個節點，或選取 [ **免費** ] 或 [ **無 \_ 可用**] 或 [每一組] 中的其中一個。 當您指定一個以上的選項時，請以逗號分隔選項。

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

指定其他選擇性的 ACF 型別屬性。 當您指定一個以上的類型屬性時，請以逗號分隔選項。

</dd> <dt>

*類型名稱* 
</dt> <dd>

指定 IDL 檔案中定義的類型。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ 配置 \]** 屬性具有下列有效的選項。



| 選項           | Description                                                           |
|------------------|-----------------------------------------------------------------------|
| **所有 \_ 節點**   | 建立一個呼叫，以針對所有節點配置和釋放記憶體。             |
| **單一 \_ 節點** | 進行許多個別呼叫，以配置和釋放每個記憶體節點。 |
| **free**         | 從伺服器 stub 傳回時釋出記憶體。                          |
| **\_免費**   | 從伺服器 stub 傳回時，不會釋放記憶體。                  |



 

根據預設，存根可以針對每個指標個別呼叫 [**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md) 和 [**midl \_ 使用者 \_**](midl-user-free-1.md) ，來為唯一或完整指標所參考的資料配置儲存區。

您可以藉由指定 **all \_ 節點** 選項來優化應用程式的速度。 此選項會指示存根計算透過指定類型的指標所參考的所有記憶體大小，以及對 [**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md)進行單一呼叫。 存根會藉由對 [**midl \_ 使用者 \_ 免費**](midl-user-free-1.md)進行一次呼叫來釋放記憶體。

Not **\_ free** 選項會指示 MIDL 編譯器產生不會針對指定的型別呼叫 [**MIDL \_ 使用者 \_ free**](midl-user-free-1.md) 的伺服器 stub。 [ **無 \_ 可用** ] 選項允許在遠端程序呼叫完成並傳回用戶端之後，讓伺服器應用程式能夠存取指標結構。

**\[ 配置 \]** 屬性將會導致任何 **\[ in、out \]** 參數（其為以 [**所有 \_ 節點**] 選項限定的型別指標），以在資料取消封送處理時重新配置記憶體。 應用程式必須負責釋放先前為此參數所配置的記憶體。 例如：

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

資料類型 PTHISTYPE 會在封送之前由存根以 [**\[ 輸出 \]**](out-idl.md)方向重新配置。 因此，應用程式必須釋放先前為此參數資料配置的記憶體，否則會發生記憶體流失。

## <a name="examples"></a>範例

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md)
</dt> <dt>

[**midl \_ 使用者 \_ 免費**](midl-user-free-1.md)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> <dt>

[**著**](typedef.md)
</dt> </dl>

 

 




