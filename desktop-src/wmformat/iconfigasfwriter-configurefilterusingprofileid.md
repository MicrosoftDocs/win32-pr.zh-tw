---
title: IConfigAsfWriter ConfigureFilterUsingProfileId 方法
description: ConfigureFilterUsingProfileId 方法會設定篩選器，以從系統組態檔案清單中，使用設定檔識別碼 (識別碼) 索引來寫入 ASF 檔案。 僅適用于 Windows Media Format 4.0 設定檔的 (。 ) 。
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
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966463"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a>IConfigAsfWriter：： ConfigureFilterUsingProfileId 方法

**ConfigureFilterUsingProfileId** 方法會設定篩選器，以從系統組態檔案清單中，使用設定檔識別碼 (識別碼) 索引來寫入 ASF 檔案。 僅適用于 Windows Media Format 4.0 設定檔的 (。 ) 

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

Windows Media 格式 SDK 4.0 版中所定義的設定檔識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                         | Description                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 此方法已成功。<br/>        |
| <dl> <dt>**E \_ 失敗**</dt> </dl>              | 設定檔無效。<br/>    |
| <dl> <dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt> </dl> | 篩選圖形已停止。<br/> |



 

## <a name="remarks"></a>備註

此方法現在已過時，因為它採用4.0 版 Windows Media Format SDK 設定檔。 若要設定7.0 和更新版本設定檔的篩選，請使用 [**IConfigAsfWriter：： ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) 或 [**IConfigAsfWriter：： ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

