---
description: 取得未壓縮像素格式的清單，這些格式可使用指定的 DirectX Video 加速 (DXVA) 設定檔來呈現。
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'IDirect3DVideoDevice9：： GetUncompressedDXVAFormats 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319007"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a>IDirect3DVideoDevice9：： GetUncompressedDXVAFormats 方法

取得未壓縮像素格式的清單，這些格式可使用指定的 DirectX Video 加速 (DXVA) 設定檔來呈現。

## <a name="syntax"></a>語法


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pGuid* 
</dt> <dd>

指定 DXVA 設定檔之 GUID 的指標。 若要取得支援的配置檔案清單，請呼叫 [**IDirect3DVideoDevice9：： GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md)。

</dd> <dt>

*pNumFormats* 
</dt> <dd>

在 [輸入] 上，指定 *pFormats* 陣列中的元素數目。 如果 *pFormats* 為 **Null**，的值 `*pNumFormats` 必須是零。

在輸出中，如果 *pFormats* 為 **Null**，則 *pNumFormats* 會接收支援的像素格式數目。 否則， *pNumFormats* 會接收復制到 *pFormats* 陣列的實際像素格式數目。

</dd> <dt>

*pFormats* 
</dt> <dd>

**D3DFORMAT** 值陣列的位址，或 **Null**。 如果此值為非 **Null**，則陣列會接收像素格式的清單。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

呼叫這個方法兩次。 在第一次呼叫時，將 *pFormats* 設定為 **Null**。 *PNumFormats* 參數會接收格式的數目。 使用所需的大小來配置 **D3DFORMAT** 陣列，然後再次呼叫方法。 這次，請將 *pFormats* 設定為數組的位址。 方法會以像素格式清單來填滿陣列。

驅動程式應依喜好設定的遞減順序傳回格式，最慣用的格式最先列出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Dxva。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




