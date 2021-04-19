---
title: WMDM_STORAGE_ENUM_MODE 列舉
description: WMDM \_ 儲存體 \_ 列舉 \_ 模式列舉型別會定義如何列舉儲存體上的內容。 IWMDMStorage3 SetEnumPreference 會使用這個列舉。
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- WMDM_STORAGE_ENUM_MODE 列舉 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d886ade00289e655ae3323a70d01be96a09852b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986178"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a>WMDM \_ 儲存體 \_ 列舉 \_ 模式列舉

**WMDM \_ 儲存體 \_ 列舉 \_ 模式** 列舉型別會定義如何列舉儲存體上的內容。 [**IWMDMStorage3：： SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference)會使用這個列舉。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**原始的列舉 \_ 模式 \_**
</dt> <dd>

列舉儲存體上的內容，就像在儲存裝置的檔案系統中組織一樣。

**列舉 \_ 模式 \_ 使用 \_ 裝置 \_ PREF**

根據 *UseMetadataViews* 裝置參數所指示的裝置喜好設定，列舉儲存體上的內容。

**列舉 \_ 模式 \_ 中繼資料 \_ 視圖**

根據元資料檢視來組織內容，以列舉儲存體上的內容。

</dd> <dt>

<span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**列舉 \_ 模式 \_ 使用 \_ 裝置 \_ PREF**
</dt> <dd>

根據 *UseMetadataViews* 裝置參數所指示的裝置喜好設定，列舉儲存體上的內容。

**列舉 \_ 模式 \_ 中繼資料 \_ 視圖**

根據元資料檢視來組織內容，以列舉儲存體上的內容。

</dd> <dt>

<span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**列舉 \_ 模式 \_ 中繼資料 \_ 視圖**
</dt> <dd>

根據元資料檢視來組織內容，以列舉儲存體上的內容。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](enumeration-types.md)
</dt> </dl>

 

 





