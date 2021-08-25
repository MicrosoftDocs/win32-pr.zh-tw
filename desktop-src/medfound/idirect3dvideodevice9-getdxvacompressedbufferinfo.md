---
description: 取得硬體加速解碼所需之壓縮緩衝區的相關資訊。
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: 'IDirect3DVideoDevice9：： GetDXVACompressedBufferInfo 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: efb96ec457cdb81f89982947bf1b9bc40543789b2e9ac253d83c81727f1efae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942288"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a>IDirect3DVideoDevice9：： GetDXVACompressedBufferInfo 方法

取得硬體加速解碼所需之壓縮緩衝區的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
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

*pNumBuffers* 
</dt> <dd>

在 [輸入] 上，指定 *pBufferInfo* 陣列中的元素數目。 如果 *pBufferInfo* 為 **Null**，的值 `*pNumBuffers` 必須是零。

在輸出中，如果 *pBufferInfo* 為 **Null**，則 *pNumBuffers* 會接收要配置的陣列大小。 否則， *pNumBuffers* 會接收復制到 *pBufferInfo* 陣列的實際元素數目。

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

[**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo)結構陣列的位址或 **Null**。 如果此值為非 **Null**，則方法會將 **DXVACompBufferInfo** 結構清單複製到這個陣列。 每個結構都對應于影片加速器所使用的一種壓縮資料緩衝區。

呼叫這個方法之前，請先將所有陣列元素設定為零。

每個陣列索引都對應至 DXVA 中定義的其中一個 DXVA 介面類別型。 影片加速器會傳回 **DXVA \_ NUM \_ 類型的 \_ 複合 \_ 緩衝區** 陣列專案清單。 如需詳細資訊，請參閱 [DXVA 1.0 規格](/windows-hardware/drivers/display/directx-video-acceleration)，第3.4 節「緩衝區描述清單」。 如果 DXVA 設定檔沒有使用特定的緩衝區類型，則該索引的專案會包含所有值的零。

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

 

 
