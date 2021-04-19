---
description: Start 方法會啟動 capture。
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: 'IESP：： Start 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d9fc3a75fc82964f6fc5a5660ef77414ae065d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983574"
---
# <a name="iespstart-method"></a>IESP：： Start 方法

**Start** 方法會啟動 capture。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFileName* \[擴展\]
</dt> <dd>

用來儲存網路資料之 [*捕獲*](c.md) 檔案的名稱指標。 如果需要日後參考，請務必快取此檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                           | Description                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt> </dl> | 此捕獲已暫停，必須先停止，才能重新開機。 呼叫 [IESP：： stop](iesp-stop.md) 以停止捕捉。<br/> |
| <dl> <dt>**NMERR \_ 捕獲**</dt> </dl>       | 已啟動 capture。<br/>                                                                                             |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>  | NPP 未連接到網路。 呼叫 [IESP：： connect](iesp-connect.md) 以將 NPP 連接到網路。<br/>          |
| <dl> <dt>**NMERR \_ 非 \_ ESP**</dt> </dl>        | NPP 已連接到網路，但不是使用 [IESP：： Connect](iesp-connect.md) 方法。<br/>                              |



 

## <a name="remarks"></a>備註

在 Windows 登錄中指定了 [*capture*](c.md) 檔案的位置，但您可以使用網路監視器來變更目錄位置。

當您使用 IESP：： Start 和 [IESP：： Stop](iesp-stop.md) 方法重新開機捕捉時，您必須呼叫 [IESP：： Configure](iesp-configure.md) 方法，以在每次呼叫 IESP：： start 重新開機捕獲資料時重新設定連接。 當您使用這三種方法來啟動和停止捕捉時，每次啟動捕獲時都會建立新的捕獲檔案。

> [!Note]  
> 您也可以使用 [IESP：:P ause](iesp-pause.md) 和 [IESP：： Resume](iesp-resume.md) 方法來啟動和停止捕捉。 使用這兩種方法時，所捕獲的資料會儲存在相同的捕獲檔案中。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP：： Configure](iesp-configure.md)
</dt> <dt>

[IESP：： Connect](iesp-connect.md)
</dt> <dt>

[IESP：:P ause](iesp-pause.md)
</dt> <dt>

[IESP：： Resume](iesp-resume.md)
</dt> <dt>

[IESP：： Stop](iesp-stop.md)
</dt> </dl>

 

 




