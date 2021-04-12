---
title: Win32_RDMSVirtualDesktopCollection 類別的 SetInt32Property 方法
description: 更新虛擬桌面集合的整數屬性。
ms.assetid: 2ea27385-5100-4e88-ad11-df5e439d0815
ms.tgt_platform: multiple
keywords:
- SetInt32Property 方法遠端桌面服務
- SetInt32Property 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，SetInt32Property 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c2a93a52ce79bc185cd37dd9ac93e5b420b5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105845"
---
# <a name="setint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="0960b-106">Win32 RDMSVirtualDesktopCollection 類別的 SetInt32Property 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0960b-106">SetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="0960b-107">更新虛擬桌面集合的整數屬性。</span><span class="sxs-lookup"><span data-stu-id="0960b-107">Updates an integer property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0960b-108">語法</span><span class="sxs-lookup"><span data-stu-id="0960b-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="0960b-109">參數</span><span class="sxs-lookup"><span data-stu-id="0960b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0960b-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0960b-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0960b-111">識別要更新之屬性的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0960b-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="0960b-112">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0960b-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0960b-113">新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="0960b-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0960b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0960b-114">Return value</span></span>

<span data-ttu-id="0960b-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0960b-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0960b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0960b-116">Requirements</span></span>



| <span data-ttu-id="0960b-117">需求</span><span class="sxs-lookup"><span data-stu-id="0960b-117">Requirement</span></span> | <span data-ttu-id="0960b-118">值</span><span class="sxs-lookup"><span data-stu-id="0960b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0960b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0960b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0960b-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="0960b-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0960b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0960b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0960b-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0960b-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="0960b-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="0960b-123">Namespace</span></span><br/>                | <span data-ttu-id="0960b-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="0960b-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0960b-125">MOF</span><span class="sxs-lookup"><span data-stu-id="0960b-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0960b-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="0960b-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0960b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0960b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0960b-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0960b-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="0960b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0960b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0960b-130">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="0960b-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





