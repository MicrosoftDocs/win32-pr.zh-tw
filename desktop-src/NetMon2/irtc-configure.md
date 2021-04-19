---
description: 提交資料捕獲的設定資料。
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'IRTC：： Configure 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 702a3883acdbb7509d79e76d8fcc73af1e167e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972620"
---
# <a name="irtcconfigure-method"></a>IRTC：： Configure 方法

Configure 方法會提交資料捕獲的 [**設定**](configure.md) 資料。

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

錯誤 BLOB 的控制碼，其中包含其他錯誤資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                                         | Description                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ BLOB \_ 未 \_ 初始化**</dt> </dl>        | 尚未呼叫 **CreateBlob** 方法。<br/>                                                                                                                                                 |
| <dl> <dt>**NMERR \_ 不正確 \_ BLOB**</dt> </dl>                 | 指向的物件不是 BLOB。<br/>                                                                                                                                                           |
| <dl> <dt>**NMERR \_ 上層 \_ BLOB**</dt> </dl>                 | BLOB 版本號碼不正確。<br/>                                                                                                                                                          |
| <dl> <dt>**NMERR \_ BLOB \_ 專案 \_ 已 \_ 存在**</dt> </dl>  | BLOB 重複。<br/>                                                                                                                                                                                |
| <dl> <dt>**NMERR \_ BLOB \_ 專案 \_ 不 \_ \_ 存在**</dt> </dl> | *HConfigurationBlob* 所指定的設定 BLOB 缺少執行這項作業所需的專案。 查看 *hErrorBlob* 傳回的錯誤 BLOB，以判斷找不到哪個專案。<br/> |
| <dl> <dt>**NMERR 不 \_ 明確的 \_ 規範**</dt> </dl>          | 遺漏 BLOB 擁有者或類別資料。<br/>                                                                                                                                                    |
| <dl> <dt>**\_ \_ \_ \_ 找不到 NMERR BLOB 擁有者**</dt> </dl>       | 找不到 BLOB 擁有者區段。<br/>                                                                                                                                                          |
| <dl> <dt>**\_ \_ \_ \_ 找不到 NMERR BLOB 類別**</dt> </dl>    | 找不到 BLOB 類別區段。<br/>                                                                                                                                                       |
| <dl> <dt>**NMERR \_ 未知 \_ 類別**</dt> </dl>             | 找到 BLOB 類別區段，但無法理解。<br/>                                                                                                                                       |
| <dl> <dt>**NMERR \_ 未知 \_ 標記**</dt> </dl>                  | 找到 BLOB 標記區段，但無法理解。<br/>                                                                                                                                            |
| <dl> <dt>**NMERR \_ BLOB \_ 轉換 \_ 錯誤**</dt> </dl>       | BLOB 已損毀。<br/>                                                                                                                                                                           |
| <dl> <dt>**NMERR 不 \_ 合法的 \_ 觸發程式**</dt> </dl>              | BLOB 的觸發程式部分已損毀。<br/>                                                                                                                                                    |
| <dl> <dt>**NMERR \_ BLOB \_ 字串 \_ 無效**</dt> </dl>         | 字串不是以 null 結束。<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>備註

您必須套用此方法來重新開機已啟動、已停止但未中斷連線的 NPP。

*HErrorBlob* 所傳回的錯誤 BLOB 包含網路監視器在 *hConfigurationBlob* 中指定的設定 BLOB 中無法瞭解或尋找的專案。 傳回的錯誤 BLOB 包含應用程式可用於進行疑難排解的錯誤資料。 例如，如果傳回 NMERR \_ BLOB \_ 專案不存在，則會在 \_ \_ \_ 傳回的錯誤 BLOB 中包含網路監視器找不到的專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC：： Connect](irtc-connect.md)
</dt> <dt>

[網路監視器 BLOB](network-monitor-blobs.md)
</dt> </dl>

 

 




