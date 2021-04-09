---
title: Win32_RDSHServer 類別的 SetInt32Property 方法
description: 更新 Win32 RDSHServer 物件的整數屬性值 \_ 。
ms.assetid: fa8df023-120d-4174-adc1-868f08fdce56
ms.tgt_platform: multiple
keywords:
- SetInt32Property 方法遠端桌面服務
- SetInt32Property 方法遠端桌面服務，Win32_RDSHServer 類別
- Win32_RDSHServer 類別遠端桌面服務，SetInt32Property 方法
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c22c8da9c046e0a42a6ec41f6ad5b3073c8d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685857"
---
# <a name="setint32property-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="a2672-106">Win32 RDSHServer 類別的 SetInt32Property 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a2672-106">SetInt32Property method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="a2672-107">更新 [**Win32 \_ RDSHServer**](win32-rdshserver.md) 物件的整數屬性值。</span><span class="sxs-lookup"><span data-stu-id="a2672-107">Updates an integer property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2672-108">語法</span><span class="sxs-lookup"><span data-stu-id="a2672-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="a2672-109">參數</span><span class="sxs-lookup"><span data-stu-id="a2672-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2672-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2672-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2672-111">識別要更新之屬性的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a2672-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="a2672-112">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2672-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2672-113">新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="a2672-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2672-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2672-114">Return value</span></span>

<span data-ttu-id="a2672-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a2672-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2672-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2672-116">Requirements</span></span>



| <span data-ttu-id="a2672-117">需求</span><span class="sxs-lookup"><span data-stu-id="a2672-117">Requirement</span></span> | <span data-ttu-id="a2672-118">值</span><span class="sxs-lookup"><span data-stu-id="a2672-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2672-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2672-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a2672-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="a2672-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a2672-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2672-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a2672-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2672-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a2672-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="a2672-123">Namespace</span></span><br/>                | <span data-ttu-id="a2672-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="a2672-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a2672-125">MOF</span><span class="sxs-lookup"><span data-stu-id="a2672-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2672-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2672-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2672-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a2672-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2672-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2672-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a2672-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2672-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2672-130">**Win32 \_ RDSHServer**</span><span class="sxs-lookup"><span data-stu-id="a2672-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





