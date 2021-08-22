---
description: 將設定檔的變更儲存至磁片。
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'IScanProfile：： Save 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 7cf4201a0d149c7b529e595d7f2c2ea92a6010f6cffd3e6c5c74fb3cdc040651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450918"
---
# <a name="iscanprofilesave-method"></a>IScanProfile：： Save 方法

將設定檔的變更儲存至磁片。

## <a name="syntax"></a>語法


```C++
HRESULT Save();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

儲存的掃描設定檔是儲存在% USERPROFILE% \\ Application Data \\ Microsoft \\ Document CENTER UserScanProfiles 的 XML 檔案 \\ 。

如果有一個以上的進程寫入 [**IScanProfile**](-wia-iscanprofile.md) 物件，則呼叫 **IScanProfile：： Save** last 的進程是唯一儲存變更的進程。

**IScanProfile：： Save** 方法會先驗證設定檔，然後再儲存。 設定檔一律會被視為有效，除非與設定檔相關聯的 Windows 映像取得 (wia) 2.0 專案是 wia \_ 類別的 \_ 平板類別或 wia \_ 類別 \_ 送紙器。 如果分類為 [WIA \_ 類別] \_ 或 \_ [wia 類別]，則 \_ 如果屬性包含在設定檔中，則下列屬性必須對專案有效：

WIA \_ IP \_ 亮度

WIA \_ IP \_ 對比

WIA \_ IPA \_ 資料類型

WIA \_ IP \_ XRES

WIA \_ IPA \_ 格式

此外，如果類別是 WIA \_ 類別 \_ 送紙器，則 [wia \_ ip \_ 頁面大小] \_ 屬性必須是有效的，如果設定檔中有此屬性的話。 如需這些屬性的詳細資訊，請參閱 [**掃描器 WIA 專案屬性常數**](-wia-wiaitempropscanneritem.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Scanprofile。h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




