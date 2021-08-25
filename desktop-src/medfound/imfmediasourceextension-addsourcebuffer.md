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
ms.openlocfilehash: b49a7c4fb0cb9e45ab0c2823d92ceb6e4076dfcaef4d2e8450f1f3d07f474279
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942028"
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
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




