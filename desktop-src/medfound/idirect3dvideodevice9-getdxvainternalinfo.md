---
description: 查詢硬體抽象層 (HAL) 將配置給其私用的記憶體數量。
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: 'IDirect3DVideoDevice9：： GetDXVAInternalInfo 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: dd15dfdbd35db56262487482e811210970852dcee4e791d710e0551b84e9e620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777208"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a>IDirect3DVideoDevice9：： GetDXVAInternalInfo 方法

查詢硬體抽象層 (HAL) 將配置給其私用的記憶體數量。

## <a name="syntax"></a>語法


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pGuid* 
</dt> <dd>

指定 DXVA 設定檔之 GUID 的指標。 若要取得支援的配置檔案清單，請呼叫 [**IDirect3DVideoDevice9：： GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md)。

</dd> <dt>

*pUncompData* 
</dt> <dd>

[**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)結構的指標，指定未壓縮資料的大小和像素格式。

</dd> <dt>

*pMemoryUsed* 
</dt> <dd>

接收 HAL 將配置的臨時記憶體量（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Dxva。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




