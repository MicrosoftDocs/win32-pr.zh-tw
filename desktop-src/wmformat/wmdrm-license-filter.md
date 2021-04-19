---
title: 'WMDRM_LICENSE_FILTER 結構 (Wmdrmsdk .h) '
description: WMDRM \_ 授權 \_ 篩選結構會定義要在建立授權列舉時使用的篩選參數。
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- WMDRM_LICENSE_FILTER 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995683"
---
# <a name="wmdrm_license_filter-structure"></a><span data-ttu-id="c7609-105">WMDRM \_ 授權 \_ 篩選結構</span><span class="sxs-lookup"><span data-stu-id="c7609-105">WMDRM\_LICENSE\_FILTER structure</span></span>

<span data-ttu-id="c7609-106">**WMDRM \_ 授權 \_ 篩選** 結構會定義要在建立授權列舉時使用的篩選參數。</span><span class="sxs-lookup"><span data-stu-id="c7609-106">The **WMDRM\_LICENSE\_FILTER** structure defines filtering parameters for use when creating a license enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7609-107">語法</span><span class="sxs-lookup"><span data-stu-id="c7609-107">Syntax</span></span>


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a><span data-ttu-id="c7609-108">成員</span><span class="sxs-lookup"><span data-stu-id="c7609-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7609-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="c7609-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c7609-110">指定所傳回授權的最小版本號碼。</span><span class="sxs-lookup"><span data-stu-id="c7609-110">Specifies a minimum version number for the returned licenses.</span></span>

</dd> <dt>

<span data-ttu-id="c7609-111">**bstrKID**</span><span class="sxs-lookup"><span data-stu-id="c7609-111">**bstrKID**</span></span>
</dt> <dd>

<span data-ttu-id="c7609-112">指定用來篩選授權的金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7609-112">Specifies a key ID to filter licenses for.</span></span> <span data-ttu-id="c7609-113">列舉中只會包含具有指定金鑰識別碼的授權。</span><span class="sxs-lookup"><span data-stu-id="c7609-113">Only licenses with the specified key ID will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="c7609-114">**bstrRights**</span><span class="sxs-lookup"><span data-stu-id="c7609-114">**bstrRights**</span></span>
</dt> <dd>

<span data-ttu-id="c7609-115">指定要篩選授權的一組許可權。</span><span class="sxs-lookup"><span data-stu-id="c7609-115">Specifies a set of rights to filter licenses for.</span></span> <span data-ttu-id="c7609-116">列舉中只會包含提供所有指定許可權的授權。</span><span class="sxs-lookup"><span data-stu-id="c7609-116">Only licenses that provide all of the specified rights will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="c7609-117">**bstrAllowedSourceIDs**</span><span class="sxs-lookup"><span data-stu-id="c7609-117">**bstrAllowedSourceIDs**</span></span>
</dt> <dd>

<span data-ttu-id="c7609-118">指定要包含在授權搜尋中的受保護內容來源。</span><span class="sxs-lookup"><span data-stu-id="c7609-118">Specifies the sources of protected content to include in the license search.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7609-119">備註</span><span class="sxs-lookup"><span data-stu-id="c7609-119">Remarks</span></span>

<span data-ttu-id="c7609-120">此結構是由 [**IWMDRMLicenseManagement：： CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="c7609-120">This structure is used by the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7609-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7609-121">Requirements</span></span>



| <span data-ttu-id="c7609-122">需求</span><span class="sxs-lookup"><span data-stu-id="c7609-122">Requirement</span></span> | <span data-ttu-id="c7609-123">值</span><span class="sxs-lookup"><span data-stu-id="c7609-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7609-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c7609-124">Header</span></span><br/> | <dl> <span data-ttu-id="c7609-125"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7609-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7609-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7609-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7609-127">**結構**</span><span class="sxs-lookup"><span data-stu-id="c7609-127">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





