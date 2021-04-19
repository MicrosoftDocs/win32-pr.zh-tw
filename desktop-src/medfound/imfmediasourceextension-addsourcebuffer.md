---
description: 將 IMFSourceBuffer 新增至與 IMFMediaSourceExtension 相關聯的緩衝區集合。
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: IMFMediaSourceExtension：： AddSourceBuffer 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.AddSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: a62a62d8cf11afaa0190ac442f84b00cfe23517b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982798"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a>IMFMediaSourceExtension：： AddSourceBuffer 方法

將 [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) 新增至與 [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)相關聯的緩衝區集合。

## <a name="syntax"></a>語法


```C++
HRESULT AddSourceBuffer(
  [in]  BSTR                  type,
  [in]  IMFSourceBufferNotify *pNotify,
  [out] IMFSourceBuffer       **ppSourceBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* \[在\]
</dt> <dd></dd> <dt>

*pNotify* \[在\]
</dt> <dd></dd> <dt>

*ppSourceBuffer* \[擴展\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




