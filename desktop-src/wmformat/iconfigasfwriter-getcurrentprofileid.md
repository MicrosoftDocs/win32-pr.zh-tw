---
title: IConfigAsfWriter GetCurrentProfileId 方法
description: GetCurrentProfileId 方法會抓取目前的設定檔識別碼。 僅適用于 Windows Media Format 4.0 設定檔的 (。 ) 。
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- GetCurrentProfileId 方法 windows Media 格式
- GetCurrentProfileId 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，GetCurrentProfileId 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967676"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a>IConfigAsfWriter：： GetCurrentProfileId 方法

**GetCurrentProfileId** 方法會抓取目前的設定檔識別碼。 僅適用于 Windows Media Format 4.0 設定檔的 (。 ) 

## <a name="syntax"></a>語法


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdwProfileId* \[擴展\]
</dt> <dd>

接收目前設定檔識別碼之 **DWORD** 類型變數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，則會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

此方法現在已過時，因為它採用4.0 版 Windows Media Format SDK 設定檔。 請改用 [**IConfigAsfWriter：： GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) 或 [**IConfigAsfWriter：： GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) ，以正確識別7.0 版和更新版本的設定檔。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 