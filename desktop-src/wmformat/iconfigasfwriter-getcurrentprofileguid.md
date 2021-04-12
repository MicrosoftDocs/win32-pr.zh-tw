---
title: IConfigAsfWriter GetCurrentProfileGuid 方法
description: GetCurrentProfileGuid 方法會抓取目前的 Windows Media system 設定檔 GUID。
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- GetCurrentProfileGuid 方法 windows Media 格式
- GetCurrentProfileGuid 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，GetCurrentProfileGuid 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316126"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>IConfigAsfWriter：： GetCurrentProfileGuid 方法

**GetCurrentProfileGuid** 方法會抓取目前的 Windows Media system 設定檔 GUID。

## <a name="syntax"></a>語法


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pProfileGuid* \[擴展\]
</dt> <dd>

**GUID** 類型變數的指標，可識別篩選所使用的目前系統設定檔。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，則會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個方法不會與自訂設定檔搭配使用 (包括包含使用 Windows Media 音訊和影片編解碼器) 之資料流程的所有設定檔，因為所有這類設定檔都是由應用程式所建立，而且沒有 GUID 識別碼。 如果未載入任何系統設定檔， *pProfileGuid* 會設為 **Null**。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 