---
title: 'ID3DX11ThreadPump GetQueueStatus 方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 取得執行緒抽取內三個佇列中的專案數。
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- GetQueueStatus 方法 Direct3D 11
- GetQueueStatus 方法 Direct3D 11，ID3DX11ThreadPump 介面
- ID3DX11ThreadPump 介面 Direct3D 11，GetQueueStatus 方法
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41535dba7c5abb96c132714ecbc6ee4e02f1f42fcb6a45ebe8795286d8613c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851498"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a>ID3DX11ThreadPump：： GetQueueStatus 方法

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

取得執行緒抽取內三個佇列中的專案數。

## <a name="syntax"></a>語法


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pIoQueue* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)\***

I/o 佇列中的專案數。

</dd> <dt>

*pProcessQueue* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)\***

進程佇列中的專案數。

</dd> <dt>

*pDeviceQueue* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)\***

裝置佇列中的專案數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

