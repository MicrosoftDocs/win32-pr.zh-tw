---
description: 執行 DirectX Video 加速 (DXVA) 解碼作業。
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'IDirect3DDXVADevice9：： Execute 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974410"
---
# <a name="idirect3ddxvadevice9execute-method"></a>IDirect3DDXVADevice9：： Execute 方法

執行 DirectX Video 加速 (DXVA) 解碼作業。

## <a name="syntax"></a>語法


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FunctionNum* 
</dt> <dd>

包含一或多個 DXVA 函式編號的 **DWORD** 。 如需詳細資訊，請參閱 [DXVA 1.0 規格](/windows-hardware/drivers/display/directx-video-acceleration)。

</dd> <dt>

*pInputData* 
</dt> <dd>

緩衝區的指標，此緩衝區包含解碼作業的輸入資料。 這項資料的意義取決於介面型別和函式編號。

</dd> <dt>

*InputSize* 
</dt> <dd>

輸入資料的大小（以位元組為單位）。

</dd> <dt>

*OutputData* 
</dt> <dd>

影片加速器寫入輸出資料之緩衝區的指標。

</dd> <dt>

*OutputSize* 
</dt> <dd>

*OutputData* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*NumBuffers* 
</dt> <dd>

*PBufferInfo* 陣列中的元素數目。

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

[**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)結構陣列的指標。

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

 

 
