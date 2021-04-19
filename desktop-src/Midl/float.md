---
title: float 屬性
description: Float 關鍵字會指定32位浮點數。
ms.assetid: dfc94378-13a4-4d34-a254-7ff68f4f9d40
keywords:
- float 屬性 MIDL
topic_type:
- apiref
api_name:
- float
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82d298506c5117c0643df8ecea841832d5f923
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106976330"
---
# <a name="float-attribute"></a>float 屬性

**Float** 關鍵字會指定32位浮點數。

``` syntax
float identifier-name;
```

## <a name="parameters"></a>參數

<dl> <dt>

*識別碼-名稱* 
</dt> <dd>

指定有效的 MIDL 識別碼。 有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。

</dd> </dl>

## <a name="remarks"></a>備註

**Float** 類型是介面定義語言 (IDL) 的其中一種基底類型。 **Float** 型別可以在 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範和參數類型指定名稱) 。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

**Float** 型別不能出現在 [**const**](const.md)宣告中。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**double**](double.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**著**](typedef.md)
</dt> </dl>

 

 




