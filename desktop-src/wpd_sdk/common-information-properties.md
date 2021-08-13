---
description: Windows可攜式裝置支援下列常見的資訊屬性。
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: '一般資訊屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41a8845a41714ed1a775d19e14f0996aad698aaf99de18da4eceb4df92688409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431101"
---
# <a name="common-information-properties"></a>一般資訊屬性

Windows可攜式裝置支援下列常見的資訊屬性。



| 屬性                                      | VarType        | 描述                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| **WPD \_ 一般 \_ 資訊 \_ 注意事項**           | **VT \_ LPWSTR** | 對於約會、工作和類似的物件，此屬性包含指定物件的任何附注。     |
| **WPD \_ 一般 \_ 資訊 \_ 主體**         | **VT \_ LPWSTR** | 值，指定這個物件的主旨欄位。                                                 |
| **WPD \_ 一般 \_ 資訊 \_ 主體 \_ 文字**      | **VT \_ LPWSTR** | 這個屬性包含純文字或 HTML 格式之物件的內文文字。                          |
| **WPD \_ 一般 \_ 資訊 \_ 優先順序**        | **VT \_ UI4**    | 值，指定這個物件的優先權。 0表示最高優先順序。                    |
| **WPD \_ 一般 \_ 資訊 \_ 開始 \_ 日期時間** | **VT \_ 日期**   | 值，指定約會、工作或類似物件排定開始的日期/時間。 |
| **WPD \_ COMMON \_ INFORMATION \_ END \_ DATETIME**   | **VT \_ 日期**   | 值，指定約會、工作或類似物件排定結束的日期/時間。   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




