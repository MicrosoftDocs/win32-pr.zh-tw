---
description: Configure 方法會提交 capture 的設定資訊。
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'IESP：： Configure 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5ae0fba6885db46d987e59517cdc30dab484974869c67c85a257044e5eec58b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365667"
---
# <a name="iespconfigure-method"></a>IESP：： Configure 方法

Configure 方法會提交 capture 的 **設定** 資訊。

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

呼叫端所設定之 BLOB 的控制碼。

</dd> <dt>

*hErrorBlob* \[擴展\]
</dt> <dd>

錯誤 BLOB 的控制碼，其中包含其他錯誤資訊。 如需錯誤 BLOB 內容的相關資訊，請參閱本主題中的「備註」一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                                         | Description                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>                | NPP 未連接到網路。<br/>                                                                                                                                                               |
| <dl> <dt>**NMERR \_ 非 \_ ESP**</dt> </dl>                      | NPP 是連接到網路，但不是使用[IESP：：連線](iesp-connect.md)方法。<br/>                                                                                                         |
| <dl> <dt>**NMERR \_ 捕獲**</dt> </dl>                     | NPP 會報告 capture 會話已啟動。<br/>                                                                                                                                                  |
| <dl> <dt>**NMERR 不 \_ 合法的 \_ 觸發程式**</dt> </dl>              | 設定 BLOB 的觸發程式部分已損毀。<br/>                                                                                                                                              |
| <dl> <dt>**NMERR \_ BLOB \_ 專案 \_ 不 \_ \_ 存在**</dt> </dl> | *HConfigurationBlob* 所指定的設定 BLOB 缺少執行這項作業所需的專案。 查看 *hErrorBlob* 傳回的錯誤 BLOB，以判斷找不到哪個專案。<br/> |
| <dl> <dt>**NMERR \_ BLOB \_ 轉換 \_ 錯誤**</dt> </dl>       | BLOB 已損毀。<br/>                                                                                                                                                                                   |
| <dl> <dt>**NMERR \_ BLOB \_ 未 \_ 初始化**</dt> </dl>        | 尚未呼叫 **CreateBlob** 方法。<br/>                                                                                                                                                         |
| <dl> <dt>**NMERR \_ 不正確 \_ BLOB**</dt> </dl>                 | 指向的物件不是 BLOB。<br/>                                                                                                                                                           |
| <dl> <dt>**NMERR \_ BLOB \_ 字串 \_ 無效**</dt> </dl>         | 字串不是以 null 結束。<br/>                                                                                                                                                                     |
| <dl> <dt>**NMERR \_ 上層 \_ BLOB**</dt> </dl>                 | BLOB 版本號碼不正確。<br/>                                                                                                                                                                  |
| <dl> <dt>**NMERR \_ \_ 記憶體不足 \_**</dt> </dl>               | 沒有可用的記憶體。 關閉 windows 以釋出資源。<br/>                                                                                                                                       |
| <dl> <dt>**NMERR \_ TIMEOUT**</dt> </dl>                       | 要求已逾時。<br/>                                                                                                                                                                             |



 

## <a name="remarks"></a>備註

您必須套用此方法，才能重新開機已啟動且停止但未中斷連線的 NPP。

*HErrorBlob* 參數所傳回的錯誤 BLOB 包含網路監視器無法在 *hConfigurationBlob* 中指定的設定 BLOB 中瞭解或尋找的專案。 傳回的錯誤 BLOB 包含應用程式可用於進行疑難排解的錯誤資訊。 例如，如果傳回 NMERR \_ BLOB \_ 專案不存在，則會在 \_ \_ \_ 傳回的錯誤 BLOB 中包含網路監視器找不到的專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



 

 




