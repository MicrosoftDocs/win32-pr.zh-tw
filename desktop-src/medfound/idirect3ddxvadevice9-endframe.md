---
description: 結束處理以建立解碼的圖片。
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'IDirect3DDXVADevice9：： EndFrame 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114228"
---
# <a name="idirect3ddxvadevice9endframe-method"></a>IDirect3DDXVADevice9：： EndFrame 方法

結束處理以建立解碼的圖片。

## <a name="syntax"></a>語法


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SizeMiscData* 
</dt> <dd>

*PMiscData* 所指定的緩衝區大小（以位元組為單位）。 值必須是2。

</dd> <dt>

*pMiscData* 
</dt> <dd>

包含影片加速器資料之緩衝區的指標。 這個緩衝區必須包含在 *pInputData* 參數中傳遞給 [**IDirect3DDXVADevice9：： BeginFrame**](idirect3ddxvadevice9-beginframe.md)方法的相同框架索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Dxva。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




