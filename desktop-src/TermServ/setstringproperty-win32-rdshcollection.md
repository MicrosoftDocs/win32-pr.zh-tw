---
title: 'Win32_RDSHCollection 類別的 SetStringProperty 方法 (Certenroll) '
description: 更新 Win32 RDSHCollection 物件的字串屬性值 \_ 。
ms.assetid: 6981b47a-5480-44f5-90e3-f64d439fa2aa
ms.tgt_platform: multiple
keywords:
- SetStringProperty 方法遠端桌面服務
- SetStringProperty 方法遠端桌面服務，Win32_RDSHCollection 類別
- Win32_RDSHCollection 類別遠端桌面服務，SetStringProperty 方法
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2606c195822432138ee67576db54f945c6834cfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968364"
---
# <a name="setstringproperty-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="c99c0-106">Win32 RDSHCollection 類別的 SetStringProperty 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c99c0-106">SetStringProperty method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="c99c0-107">更新 [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) 物件的字串屬性值。</span><span class="sxs-lookup"><span data-stu-id="c99c0-107">Updates a string property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c99c0-108">語法</span><span class="sxs-lookup"><span data-stu-id="c99c0-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="c99c0-109">參數</span><span class="sxs-lookup"><span data-stu-id="c99c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c99c0-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c99c0-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c99c0-111">識別要更新之屬性的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c99c0-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="c99c0-112">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c99c0-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c99c0-113">新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="c99c0-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c99c0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c99c0-114">Return value</span></span>

<span data-ttu-id="c99c0-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c99c0-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c99c0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c99c0-116">Requirements</span></span>



| <span data-ttu-id="c99c0-117">需求</span><span class="sxs-lookup"><span data-stu-id="c99c0-117">Requirement</span></span> | <span data-ttu-id="c99c0-118">值</span><span class="sxs-lookup"><span data-stu-id="c99c0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c99c0-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c99c0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c99c0-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="c99c0-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c99c0-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c99c0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c99c0-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c99c0-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c99c0-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="c99c0-123">Namespace</span></span><br/>                | <span data-ttu-id="c99c0-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="c99c0-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c99c0-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c99c0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c99c0-126"><dt>Certenroll。h</dt></span><span class="sxs-lookup"><span data-stu-id="c99c0-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="c99c0-127">MOF</span><span class="sxs-lookup"><span data-stu-id="c99c0-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c99c0-128"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="c99c0-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c99c0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c99c0-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c99c0-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c99c0-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c99c0-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c99c0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c99c0-132">**Win32 \_ RDSHCollection**</span><span class="sxs-lookup"><span data-stu-id="c99c0-132">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





