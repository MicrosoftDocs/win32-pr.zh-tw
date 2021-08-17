---
description: 取得顯示驅動程式支援 (DXVA) 設定檔的 DirectX 影片加速清單。
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'IDirect3DVideoDevice9：： GetDXVAGuids 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 6a355c27177a546a2e91e769f72d9f4b9e216b005f711d42b5b7af39b4b78361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119269238"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a>IDirect3DVideoDevice9：： GetDXVAGuids 方法

取得顯示驅動程式支援 (DXVA) 設定檔的 DirectX 影片加速清單。

## <a name="syntax"></a>語法


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNumGuids* 
</dt> <dd>

在 [輸入] 上，指定 *pGuids* 陣列中的元素數目。 如果 *pGuids* 為 **Null**，的值 `*pNumGuids` 必須是零。

在輸出時，如果 *pGuids* 為 **Null**， *PNUMGUIDS* 會收到限制模式 DXVA 設定檔的數目。 否則， *pNumGuids* 會接收復制到 *pGuids* 陣列的實際 guid 數目。

</dd> <dt>

*pGuids* 
</dt> <dd>

Guid 陣列的位址或 **Null**。 如果此值為非 **Null**，則陣列會接收指定受限制模式 DXVA 設定檔的 guid 清單。 這些 Guid 是在 dxva 中定義的，並記載于 [dxva 1.0 規格](/windows-hardware/drivers/display/directx-video-acceleration)中。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

呼叫這個方法兩次。 在第一次呼叫時，將 *pGuids* 設定為 **Null**。 *PNumGuids* 參數會接收 DXVA 設定檔 guid 的數目。 配置具有所需大小的 Guid 陣列，然後再次呼叫方法。 這次，請將 *pGuids* 設定為數組的位址。 方法會使用 DXVA 設定檔 Guid 清單來填入陣列。

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

 

 
