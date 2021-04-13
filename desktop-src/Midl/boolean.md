---
title: 布林值屬性
description: 關鍵字布林值表示與識別碼相關聯的運算式或常數運算式只接受值 TRUE 和 FALSE。
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- 布林屬性 MIDL
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373165"
---
# <a name="boolean-attribute"></a>布林值屬性

關鍵字 **布林值** 表示與識別碼相關聯的運算式或常數運算式只接受值 **TRUE** 和 **FALSE**。

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a>參數

<dl> <dt>

*識別碼-名稱* 
</dt> <dd>

指定有效的 MIDL 識別碼。 有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。

</dd> </dl>

## <a name="remarks"></a>備註

**布林值** 型別是 IDL 語言的其中一種基底類型。 **布林值** 型別可以在 [**const**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範，以及) 的參數類型指定名稱。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

> [!Note]  
> **布林值** 基底類型與 [**oleautomation**](oleautomation.md)屬性不相容。 \_在您的自動化相容介面中使用 VARIANT BOOL。

 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**著**](typedef.md)
</dt> </dl>

 

 




