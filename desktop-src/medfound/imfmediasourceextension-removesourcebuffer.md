---
description: 從 IMFMediaSourceExtension 物件所管理的來源緩衝區集合中移除指定的來源緩衝區。
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: IMFMediaSourceExtension：： RemoveSourceBuffer 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 52c15882b57191169f033ab8a3b6c2f50f10f8e20b8f081c7bc70b7509b9a58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013968"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a>IMFMediaSourceExtension：： RemoveSourceBuffer 方法

從 [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) 物件所管理的來源緩衝區集合中移除指定的來源緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSourceBuffer* \[在\]
</dt> <dd>

要移除的緩衝區。

</dd> </dl>

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

 

 




