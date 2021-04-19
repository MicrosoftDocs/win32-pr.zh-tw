---
description: WPD \_ 參數 \_ 使用 \_ 類型列舉類型會描述如何在指定方法中使用方法參數。
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: 'WPD_PARAMETER_USAGE_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994659"
---
# <a name="wpd_parameter_usage_types-enumeration"></a>WPD \_ 參數 \_ 使用 \_ 類型列舉

[**WPD \_ 參數 \_ 使用 \_ 類型**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types)列舉類型會描述如何在指定方法中使用方法參數。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**WPD \_ 參數 \_ 使用方式傳回 \_**
</dt> <dd>

參數會接收傳回值（如果是由方法指定）。

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**WPD \_ 參數 \_ 使用 \_ 方式**
</dt> <dd>

參數會在呼叫方法之前包含輸入值。

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**WPD \_ 參數 \_ 使用 \_ 方式**
</dt> <dd>

此參數包含方法傳回時的輸出值。

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**WPD \_ 參數 \_ 使用方式 \_ INOUT**
</dt> <dd>

參數包含在呼叫方法之前的輸入值，以及傳回時的輸出值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



 

