---
title: IConfigAsfWriter GetCurrentProfile 方法
description: GetCurrentProfile 方法會抓取應用程式定義的設定檔。
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- GetCurrentProfile 方法 windows Media 格式
- GetCurrentProfile 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，GetCurrentProfile 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b7a07ed6ab5b94138c0c04d40782496535e0ae4a3eff0f443c89d7ccd0c4b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198379"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a>IConfigAsfWriter：： GetCurrentProfile 方法

**GetCurrentProfile** 方法會抓取應用程式定義的設定檔。

## <a name="syntax"></a>語法


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppProfile* \[擴展\]
</dt> <dd>

接收應用程式定義設定檔之 [**IWMProfile**](iwmprofile.md) 介面的指標位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，則會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果方法成功，則傳回的 **IWMProfile** 指標有未處理的參考計數。 使用完畢後，請務必釋放介面。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 