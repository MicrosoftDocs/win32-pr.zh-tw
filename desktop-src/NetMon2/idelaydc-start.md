---
description: IDelaydC：： Start 方法-Start 方法會啟動 capture。
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'IDelaydC：： Start 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 25bf778d9cccce20c736c5f8b83e6af9754ac933
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118436"
---
# <a name="idelaydcstart-method"></a>IDelaydC：： Start 方法

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



| 傳回碼                                                                                           | Description                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt> </dl> | 捕捉處於暫停狀態，必須先停止，才能重新開機。 呼叫 [**IDelaydC：： stop**](idelaydc-stop.md) 以停止捕捉。 如需詳細資訊，請參閱本主題中的「備註」一節。<br/> |
| <dl> <dt>**NMERR \_ 捕獲**</dt> </dl>       | 已啟動 capture。<br/>                                                                                                                                                                                 |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>  | NPP 未連接到網路。 呼叫 [**IDelaydC：： connect**](idelaydc-connect.md) 以連接到網路。<br/>                                                                                          |
| <dl> <dt>**NMERR \_ 未 \_ 延遲**</dt> </dl>    | NPP 已連接到網路，但不是使用 [**IDelaydC：： Connect**](idelaydc-connect.md) 方法。<br/>                                                                                                      |



 

## <a name="remarks"></a>備註

您可以在 Windows 登錄中指定 [*capture*](c.md) 檔案的位置，但您可以使用網路監視器來變更檔案的位置。

若要使用 **IDelaydC：： start** 和 [**IDelaydC：： Stop**](idelaydc-stop.md)重新開機 capture，您必須呼叫 [**IDelaydC：： Configure**](idelaydc-configure.md) 方法，以在每次呼叫 **IDelaydC：： start** 方法重新開機捕獲資料時重新設定連接。 當您使用這三種方法來啟動和停止捕捉時，每次啟動捕獲時都會建立新的捕獲檔案。

> [!Note]  
> 您也可以使用 [**IDelaydC：:P ause**](idelaydc-pause.md) 和 [**IDelaydC：： Resume**](idelaydc-resume.md) 方法來啟動和停止捕捉。 當您使用這兩種方法時，所捕獲的資料會儲存在相同的捕獲檔案中。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[**IDelaydC：： Configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC：： Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC：:P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC：： Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC：： Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




