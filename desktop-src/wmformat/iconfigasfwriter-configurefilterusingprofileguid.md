---
title: IConfigAsfWriter ConfigureFilterUsingProfileGuid 方法
description: ConfigureFilterUsingProfileGuid 方法會設定篩選準則，以根據指定的預先定義設定檔來寫入 ASF 檔案。  (已淘汰。 ) 。
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- ConfigureFilterUsingProfileGuid 方法 windows Media 格式
- ConfigureFilterUsingProfileGuid 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，ConfigureFilterUsingProfileGuid 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f427dc67695ebaca3e3e7502f2f1961b738a8f775ace394948ef445f3ad9a64e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118703084"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a>IConfigAsfWriter：： ConfigureFilterUsingProfileGuid 方法

**ConfigureFilterUsingProfileGuid** 方法會設定篩選準則，以根據指定的預先定義設定檔來寫入 ASF 檔案。 (已取代。)

## <a name="syntax"></a>語法


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*guidProfile* \[在\]
</dt> <dd>

識別設定檔的 **GUID** ，如 Windows 媒體格式 SDK 標頭檔 Wmsysprf. h 中所定義。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                         | 描述                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 此方法已成功。<br/>        |
| <dl> <dt>**E \_ 失敗**</dt> </dl>              | 設定檔無效。<br/>    |
| <dl> <dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt> </dl> | 篩選圖形已停止。<br/> |



 

## <a name="remarks"></a>備註

從 Windows 媒體格式9系列 SDK 開始，尚未定義任何新的系統設定檔。 只有第8版 (或較早的) 系統設定檔 Guid 可搭配此方法使用。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

