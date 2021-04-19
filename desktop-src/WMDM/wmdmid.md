---
title: WMDMID 結構
description: WMDMID 結構描述序號和群組識別碼。
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- WMDMID 結構 windows Media 裝置管理員
- PWMDMID 結構指標 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001191"
---
# <a name="wmdmid-structure"></a><span data-ttu-id="3fde0-105">WMDMID 結構</span><span class="sxs-lookup"><span data-stu-id="3fde0-105">WMDMID structure</span></span>

<span data-ttu-id="3fde0-106">**WMDMID** 結構描述序號和群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="3fde0-106">The **WMDMID** structure describes serial numbers and group IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fde0-107">語法</span><span class="sxs-lookup"><span data-stu-id="3fde0-107">Syntax</span></span>


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a><span data-ttu-id="3fde0-108">成員</span><span class="sxs-lookup"><span data-stu-id="3fde0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3fde0-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="3fde0-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="3fde0-110">**WMDMID** 結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3fde0-110">Size of the **WMDMID** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3fde0-111">**dwVendorID**</span><span class="sxs-lookup"><span data-stu-id="3fde0-111">**dwVendorID**</span></span>
</dt> <dd>

<span data-ttu-id="3fde0-112">**DWORD** ，包含廠商的註冊 ID 號碼。</span><span class="sxs-lookup"><span data-stu-id="3fde0-112">**DWORD** containing the registered ID number of the vendor.</span></span> <span data-ttu-id="3fde0-113">如果不在使用中，則包含零。</span><span class="sxs-lookup"><span data-stu-id="3fde0-113">Contains zero if not in use.</span></span>

</dd> <dt>

<span data-ttu-id="3fde0-114">**pID \[ WMDMID \_ 長度\]**</span><span class="sxs-lookup"><span data-stu-id="3fde0-114">**pID\[WMDMID\_LENGTH\]**</span></span>
</dt> <dd>

<span data-ttu-id="3fde0-115">包含序號之位元組陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="3fde0-115">Pointer to an array of bytes containing the serial number.</span></span> <span data-ttu-id="3fde0-116">序號是沒有標準格式的位元組值字串。</span><span class="sxs-lookup"><span data-stu-id="3fde0-116">The serial number is a string of byte values that have no standard format.</span></span> <span data-ttu-id="3fde0-117">請注意，這不是寬字元的值。</span><span class="sxs-lookup"><span data-stu-id="3fde0-117">Note that this is not a wide-character value.</span></span> <span data-ttu-id="3fde0-118">**WMDMID \_長度** 是在 mswmdm 中定義的常數值。</span><span class="sxs-lookup"><span data-stu-id="3fde0-118">**WMDMID\_LENGTH** is a constant value defined in mswmdm.h.</span></span>

</dd> <dt>

<span data-ttu-id="3fde0-119">**SerialNumberLength**</span><span class="sxs-lookup"><span data-stu-id="3fde0-119">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="3fde0-120">傳回之序號的實際長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3fde0-120">Actual length of the serial number returned, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3fde0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fde0-121">Requirements</span></span>



| <span data-ttu-id="3fde0-122">需求</span><span class="sxs-lookup"><span data-stu-id="3fde0-122">Requirement</span></span> | <span data-ttu-id="3fde0-123">值</span><span class="sxs-lookup"><span data-stu-id="3fde0-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3fde0-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3fde0-124">Header</span></span><br/> | <dl> <span data-ttu-id="3fde0-125"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3fde0-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fde0-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fde0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fde0-127">**IMDSPDevice::GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="3fde0-127">**IMDSPDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="3fde0-128">**IMDSPStorageGlobals::GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="3fde0-128">**IMDSPStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="3fde0-129">**IWMDMDevice::GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="3fde0-129">**IWMDMDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="3fde0-130">**IWMDMStorageGlobals::GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="3fde0-130">**IWMDMStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="3fde0-131">**結構**</span><span class="sxs-lookup"><span data-stu-id="3fde0-131">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





