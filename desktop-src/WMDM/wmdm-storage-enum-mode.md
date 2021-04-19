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
# <a name="wmdm_storage_enum_mode-enumeration"></a><span data-ttu-id="96c0b-105">WMDM \_ 儲存體 \_ 列舉 \_ 模式列舉</span><span class="sxs-lookup"><span data-stu-id="96c0b-105">WMDM\_STORAGE\_ENUM\_MODE enumeration</span></span>

<span data-ttu-id="96c0b-106">**WMDM \_ 儲存體 \_ 列舉 \_ 模式** 列舉型別會定義如何列舉儲存體上的內容。</span><span class="sxs-lookup"><span data-stu-id="96c0b-106">The **WMDM\_STORAGE\_ENUM\_MODE** enumeration type defines how the content on the storage is to be enumerated.</span></span> <span data-ttu-id="96c0b-107">[**IWMDMStorage3：： SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference)會使用這個列舉。</span><span class="sxs-lookup"><span data-stu-id="96c0b-107">This enumeration is used by [**IWMDMStorage3::SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).</span></span>

## <a name="syntax"></a><span data-ttu-id="96c0b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="96c0b-108">Syntax</span></span>


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a><span data-ttu-id="96c0b-109">常數</span><span class="sxs-lookup"><span data-stu-id="96c0b-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="96c0b-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**原始的列舉 \_ 模式 \_**</span><span class="sxs-lookup"><span data-stu-id="96c0b-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**ENUM\_MODE\_RAW**</span></span>
</dt> <dd>

<span data-ttu-id="96c0b-111">列舉儲存體上的內容，就像在儲存裝置的檔案系統中組織一樣。</span><span class="sxs-lookup"><span data-stu-id="96c0b-111">Enumerates content on the storage just as it is organized in the file system of the storage.</span></span>

<span data-ttu-id="96c0b-112">**列舉 \_ 模式 \_ 使用 \_ 裝置 \_ PREF**</span><span class="sxs-lookup"><span data-stu-id="96c0b-112">**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>

<span data-ttu-id="96c0b-113">根據 *UseMetadataViews* 裝置參數所指示的裝置喜好設定，列舉儲存體上的內容。</span><span class="sxs-lookup"><span data-stu-id="96c0b-113">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="96c0b-114">**列舉 \_ 模式 \_ 中繼資料 \_ 視圖**</span><span class="sxs-lookup"><span data-stu-id="96c0b-114">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="96c0b-115">根據元資料檢視來組織內容，以列舉儲存體上的內容。</span><span class="sxs-lookup"><span data-stu-id="96c0b-115">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="96c0b-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**列舉 \_ 模式 \_ 使用 \_ 裝置 \_ PREF**</span><span class="sxs-lookup"><span data-stu-id="96c0b-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>
</dt> <dd>

<span data-ttu-id="96c0b-117">根據 *UseMetadataViews* 裝置參數所指示的裝置喜好設定，列舉儲存體上的內容。</span><span class="sxs-lookup"><span data-stu-id="96c0b-117">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="96c0b-118">**列舉 \_ 模式 \_ 中繼資料 \_ 視圖**</span><span class="sxs-lookup"><span data-stu-id="96c0b-118">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="96c0b-119">根據元資料檢視來組織內容，以列舉儲存體上的內容。</span><span class="sxs-lookup"><span data-stu-id="96c0b-119">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="96c0b-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**列舉 \_ 模式 \_ 中繼資料 \_ 視圖**</span><span class="sxs-lookup"><span data-stu-id="96c0b-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**ENUM\_MODE\_METADATA\_VIEWS**</span></span>
</dt> <dd>

<span data-ttu-id="96c0b-121">根據元資料檢視來組織內容，以列舉儲存體上的內容。</span><span class="sxs-lookup"><span data-stu-id="96c0b-121">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96c0b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="96c0b-122">Requirements</span></span>



| <span data-ttu-id="96c0b-123">需求</span><span class="sxs-lookup"><span data-stu-id="96c0b-123">Requirement</span></span> | <span data-ttu-id="96c0b-124">值</span><span class="sxs-lookup"><span data-stu-id="96c0b-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="96c0b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="96c0b-125">Header</span></span><br/> | <dl> <span data-ttu-id="96c0b-126"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="96c0b-126"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96c0b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96c0b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c0b-128">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="96c0b-128">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





