---
title: IConfigAsfWriter ConfigureFilterUsingProfileId 方法
description: ConfigureFilterUsingProfileId 方法會設定篩選器，以從系統組態檔案清單中，使用設定檔識別碼 (識別碼) 索引來寫入 ASF 檔案。 僅適用于 Windows 媒體格式4.0 設定檔的 (。 ) 。
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- ConfigureFilterUsingProfileId 方法 windows Media 格式
- ConfigureFilterUsingProfileId 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，ConfigureFilterUsingProfileId 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6321d259a213426df7e4490c3fc8a793e583a6fcdf58ec795a9f88e43645377f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118028482"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a>IConfigAsfWriter：： ConfigureFilterUsingProfileId 方法

**ConfigureFilterUsingProfileId** 方法會設定篩選器，以從系統組態檔案清單中，使用設定檔識別碼 (識別碼) 索引來寫入 ASF 檔案。 僅適用于 Windows 媒體格式4.0 設定檔的 (。 ) 

## <a name="syntax"></a>語法


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwProfileId* \[在\]
</dt> <dd>

設定檔識別碼，如 Windows 媒體格式 SDK 4.0 版中所定義。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                         | 描述                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 此方法已成功。<br/>        |
| <dl> <dt>**E \_ 失敗**</dt> </dl>              | 設定檔無效。<br/>    |
| <dl> <dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt> </dl> | 篩選圖形已停止。<br/> |



 

## <a name="remarks"></a>備註

此方法現在已過時，因為它採用4.0 版 Windows 媒體格式 SDK 設定檔。 若要設定7.0 和更新版本設定檔的篩選，請使用 [**IConfigAsfWriter：： ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) 或 [**IConfigAsfWriter：： ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

