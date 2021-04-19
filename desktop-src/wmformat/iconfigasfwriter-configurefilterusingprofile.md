---
title: IConfigAsfWriter ConfigureFilterUsingProfile 方法
description: ConfigureFilterUsingProfile 方法是設定設定檔的建議方式。 它會根據指定的應用程式定義設定檔，設定篩選來寫入 ASF 檔案。
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- ConfigureFilterUsingProfile 方法 windows Media 格式
- ConfigureFilterUsingProfile 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，ConfigureFilterUsingProfile 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106980278"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a>IConfigAsfWriter：： ConfigureFilterUsingProfile 方法

**ConfigureFilterUsingProfile** 方法是設定設定檔的建議方式。 它會根據指定的應用程式定義設定檔，設定篩選來寫入 ASF 檔案。

## <a name="syntax"></a>語法


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pProfile* \[在\]
</dt> <dd>

應用程式定義設定檔上 [**IWMProfile**](iwmprofile.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                         | Description                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 此方法已成功。<br/>                              |
| <dl> <dt>**E \_ 指標**</dt> </dl>           | **IWMProfile** 介面指標無效。<br/> |
| <dl> <dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt> </dl> | 圖形已停止。<br/>                              |



 

## <a name="remarks"></a>備註

如果成功，這個方法會導致將 **EC \_ GRAPH \_ 變更** 事件傳送至應用程式。 您可以使用這個方法，利用 Windows Media 格式 SDK 的方法，使用您已 (建立的自訂 Windows Media 9 系列設定檔來設定寫入器，或從現有的 prx 檔案載入該設定檔) 。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

