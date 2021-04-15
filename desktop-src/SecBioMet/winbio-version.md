---
title: 'WINBIO_VERSION 結構 (Winbio \_ 類型 .h) '
description: 包含生物特徵辨識服務提供者元件的軟體版本號碼。
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- WINBIO_VERSION 結構 Windows 生物特徵辨識架構 API
- PWINBIO_VERSION 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466913"
---
# <a name="winbio_version-structure"></a><span data-ttu-id="c515f-105">WINBIO \_ 版本結構</span><span class="sxs-lookup"><span data-stu-id="c515f-105">WINBIO\_VERSION structure</span></span>

<span data-ttu-id="c515f-106">**WINBIO \_ 版本** 結構包含生物特徵辨識服務提供者元件的軟體版本號碼。</span><span class="sxs-lookup"><span data-stu-id="c515f-106">The **WINBIO\_VERSION** structure contains the software version number of a biometric service provider component.</span></span>

## <a name="syntax"></a><span data-ttu-id="c515f-107">語法</span><span class="sxs-lookup"><span data-stu-id="c515f-107">Syntax</span></span>


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a><span data-ttu-id="c515f-108">成員</span><span class="sxs-lookup"><span data-stu-id="c515f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c515f-109">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="c515f-109">**MajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c515f-110">包含主要版本號碼的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="c515f-110">A **DWORD** that contains the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="c515f-111">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="c515f-111">**MinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c515f-112">包含次要版本號碼的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="c515f-112">A **DWORD** that contains the minor version number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c515f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c515f-113">Requirements</span></span>



| <span data-ttu-id="c515f-114">需求</span><span class="sxs-lookup"><span data-stu-id="c515f-114">Requirement</span></span> | <span data-ttu-id="c515f-115">值</span><span class="sxs-lookup"><span data-stu-id="c515f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c515f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c515f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c515f-117">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c515f-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="c515f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c515f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c515f-119">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c515f-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c515f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c515f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c515f-121"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c515f-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c515f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c515f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c515f-123">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="c515f-123">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="c515f-124">**WINBIO \_ BSP \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="c515f-124">**WINBIO\_BSP\_SCHEMA**</span></span>](winbio-bsp-schema.md)
</dt> <dt>

[<span data-ttu-id="c515f-125">**WINBIO \_ 單元 \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="c515f-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





