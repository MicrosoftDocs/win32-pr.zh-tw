---
title: 'Win32_RDMSVirtualDesktopCollection 類別的 SetStringProperty 方法 (Certenroll) '
description: 更新虛擬桌面集合的字串屬性。
ms.assetid: d76d5f77-3b51-41b9-8ec5-a737ddc0a9d3
ms.tgt_platform: multiple
keywords:
- SetStringProperty 方法遠端桌面服務
- SetStringProperty 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，SetStringProperty 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fd85ef6611cd02dc80ca66816c5c4ce13f6cd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966128"
---
# <a name="setstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="cb4fe-106">Win32 RDMSVirtualDesktopCollection 類別的 SetStringProperty 方法 \_</span><span class="sxs-lookup"><span data-stu-id="cb4fe-106">SetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="cb4fe-107">更新虛擬桌面集合的字串屬性。</span><span class="sxs-lookup"><span data-stu-id="cb4fe-107">Updates a string property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb4fe-108">語法</span><span class="sxs-lookup"><span data-stu-id="cb4fe-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="cb4fe-109">參數</span><span class="sxs-lookup"><span data-stu-id="cb4fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb4fe-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb4fe-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb4fe-111">識別要更新之屬性的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="cb4fe-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="cb4fe-112">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb4fe-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb4fe-113">新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="cb4fe-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb4fe-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb4fe-114">Return value</span></span>

<span data-ttu-id="cb4fe-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cb4fe-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb4fe-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb4fe-116">Requirements</span></span>



| <span data-ttu-id="cb4fe-117">需求</span><span class="sxs-lookup"><span data-stu-id="cb4fe-117">Requirement</span></span> | <span data-ttu-id="cb4fe-118">值</span><span class="sxs-lookup"><span data-stu-id="cb4fe-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4fe-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb4fe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb4fe-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="cb4fe-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="cb4fe-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb4fe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb4fe-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cb4fe-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="cb4fe-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="cb4fe-123">Namespace</span></span><br/>                | <span data-ttu-id="cb4fe-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="cb4fe-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="cb4fe-125">標頭</span><span class="sxs-lookup"><span data-stu-id="cb4fe-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb4fe-126"><dt>Certenroll。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb4fe-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="cb4fe-127">MOF</span><span class="sxs-lookup"><span data-stu-id="cb4fe-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb4fe-128"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb4fe-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb4fe-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cb4fe-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb4fe-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb4fe-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="cb4fe-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb4fe-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb4fe-132">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="cb4fe-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





