---
title: IDWriteTextLayout3 GetLineMetrics 方法
description: 抓取每一行的屬性。
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- GetLineMetrics 方法直接寫入
- GetLineMetrics 方法 Direct Write，IDWriteTextLayout3 介面
- IDWriteTextLayout3 介面 Direct Write，GetLineMetrics 方法
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465841"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a>IDWriteTextLayout3：： GetLineMetrics 方法

抓取每一行的屬性。

## <a name="syntax"></a>語法


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lineMetrics* \[擴展\]
</dt> <dd>

要填入行資訊的陣列。

</dd> <dt>

*maxLineCount* 
</dt> <dd>

LineMetrics 陣列的大小上限。

</dd> <dt>

*actualLineCount* \[擴展\]
</dt> <dd>

所需 lineMetrics 陣列的實際大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果 maxLineCount 不夠大 \_ \_ ，就 \_ 相當於 WIN32 中的 HRESULT （相當於 \_ \_ WIN32 (錯誤的 \_ \_ 緩衝區) ），會傳回，而且 actualLineCount 會設定為所需的行數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                 |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





