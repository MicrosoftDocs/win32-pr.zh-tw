---
description: IAMTimelineSplittable 介面會將 DirectShow 編輯服務中的時間軸物件分割 (DES) 。 來源、效果、轉換和追蹤都會執行這個介面。
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: 'IAMTimelineSplittable 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7b9544809068029b4ca583e83831f9b18ac84e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981264"
---
# <a name="iamtimelinesplittable-interface"></a>IAMTimelineSplittable 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

介面會將 `IAMTimelineSplittable` [DirectShow 編輯服務](directshow-editing-services.md) 中的時間軸物件分割 (DES) 。 來源、效果、轉換和追蹤都會執行這個介面。

## <a name="members"></a>成員

**IAMTimelineSplittable** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMTimelineSplittable** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMTimelineSplittable** 介面具有這些方法。



| 方法                                             | 描述                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**SplitAt**](iamtimelinesplittable-splitat.md)   | 在指定的時間分割物件。<br/>                                                  |
| [**SplitAt2**](iamtimelinesplittable-splitat2.md) | 在指定的時間分割物件，指定為 [**REFTIME**](reftime.md) 值。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
