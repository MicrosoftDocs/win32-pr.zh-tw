---
description: 將指定的掃描設定檔設定為預設設定檔。
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'IScanProfileMgr：： SetDefault 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: fd7b46241e967e02083c344aa7f3f77a773c72b02ff74b225910788d498fe252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965787"
---
# <a name="iscanprofilemgrsetdefault-method"></a>IScanProfileMgr：： SetDefault 方法

將指定的掃描設定檔設定為預設設定檔。

## <a name="syntax"></a>語法


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pScanProfile* \[在\]
</dt> <dd>

類型： **[ **IScanProfile**](-wia-iscanprofile.md)\***

設定檔的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

使用 **IScanProfileMgr：： SetDefault** 方法，將專案新增 `<Default>` 至設定檔，或從裝置的先前預設設定檔中移除該元素。

使用 [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) 方法來變更預設設定檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Scanprofilemgr。h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




