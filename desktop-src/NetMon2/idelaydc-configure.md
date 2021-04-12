---
description: Configure 方法會提交用於捕捉的設定資訊。
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: 'IDelaydCConfigure 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468744"
---
# <a name="idelaydcconfigure-method"></a>IDelaydC：： Configure 方法

Configure 方法會提交用於捕捉的 **設定** 資訊。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hConfigurationBlob* \[在\]
</dt> <dd>

包含設定資訊之 BLOB 的控制碼。

</dd> <dt>

*hErrorBlob* \[擴展\]
</dt> <dd>

錯誤 BLOB 的控制碼，其中包含其他錯誤資訊。 如需錯誤 BLOB 內容的相關資訊，請參閱本主題中的「備註」一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                                      | Description                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 捕獲**</dt> </dl>                  | NPP 會報告 capture 會話已啟動。<br/>                          |
| <dl> <dt>**NMERR \_ 磁片 \_ 未 \_ 固定在本機 \_**</dt> </dl>    |                                                                                           |
| <dl> <dt>**NMERR \_ 無法 \_ \_ 建立 \_ 記憶體**</dt> </dl> |                                                                                           |
| <dl> <dt>**NMERR \_ \_ 記憶體不足 \_**</dt> </dl>            | 沒有可用的記憶體。 關閉 windows 以釋出資源。<br/>               |
| <dl> <dt>**NMERR \_ 不正確 \_ 參數**</dt> </dl>         | HConfiguration 參數所指定的設定 BLOB 無效。<br/> |



 

## <a name="remarks"></a>備註

您必須套用此方法來重新開機已啟動、已停止但未中斷連線的 NPP。

*HErrorBlob* 所傳回的錯誤 BLOB 包含網路監視器在 *hConfigurationBlob* 中指定的設定 BLOB 中無法瞭解或尋找的專案。 傳回的錯誤 BLOB 包含應用程式可用於進行疑難排解的錯誤資訊。 例如，如果傳回 NMERR \_ BLOB \_ 專案不存在，則會在 \_ \_ \_ 傳回的錯誤 BLOB 中包含網路監視器找不到的專案。

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

[IDelaydC：： Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC：： Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC：： Stop](idelaydc-stop.md)
</dt> </dl>

 

 




