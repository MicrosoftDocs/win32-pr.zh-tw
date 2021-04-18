---
title: double 屬性
description: Double 關鍵字會指定64位浮點數。
ms.assetid: a235e9c5-90b3-4fa4-9154-06511abcccd0
keywords:
- double 屬性 MIDL
topic_type:
- apiref
api_name:
- double
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f14f4906de9e843c9413411c9d45ba927cc40ee4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507629"
---
# <a name="double-attribute"></a>double 屬性

**Double** 關鍵字會指定64位浮點數。

``` syntax
double identifier-name;
```

## <a name="parameters"></a>參數

<dl> <dt>

*識別碼-名稱* 
</dt> <dd>

指定有效的 MIDL 識別碼。 有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。

</dd> </dl>

## <a name="remarks"></a>備註

**Double** 類型是介面定義語言 (IDL) 的其中一種基底類型。 這個型別可以在 [**typedef**](typedef.md) 宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

**Double** 型別不能出現在 [**const**](const.md)宣告中。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**浮動**](float.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**著**](typedef.md)
</dt> </dl>

 

 




