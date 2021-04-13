---
title: 'D2D1_SIZE_F (D2DBaseTypes) '
description: 儲存一組排序的浮點數，通常是矩形的寬度和高度。
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464741"
---
# <a name="d2d1_size_f"></a>D2D1 \_ 大小 \_ F

儲存一組排序的浮點數，通常是矩形的寬度和高度。


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a>備註

就像點一樣，大小是另一個重要的圖形概念。 在 Direct2D 中，大小是以 **D2D1 \_ 大小 \_ F** 或 [**D2D1 \_ 大小 \_ U**](d2d1-size-u.md) 結構表示。 兩者都包含一組已排序的數位，通常是矩形的寬度和高度。 **D2D1 \_ size \_ F** 結構包含一組排序的 **FLOAT** 值，而 **D2D1 \_ 大小 \_ U** 結構包含一對 **UINT32** 值的排序。

**D2D1 \_\_F 大小** 是已定義的類型 **D2D \_ \_ f 大小** 的新名稱。 如需 **D2D1 \_ 大小 \_ f** 所提供的欄位清單，請參閱 **D2D \_ 大小 \_ f**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]<br/>                          |
| 最低支援的伺服器<br/> | Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>D2DBaseTypes (包含 D2d1) </dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D2D \_ 大小 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[**D2D1 \_ 大小 \_ U**](d2d1-size-u.md)
</dt> <dt>

[**D2D1 \_ 點 \_ 2f**](d2d1-point-2f.md)
</dt> </dl>

 

