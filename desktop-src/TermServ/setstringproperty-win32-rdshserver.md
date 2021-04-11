---
title: 'Win32_RDSHServer 類別的 SetStringProperty 方法 (Certenroll) '
description: 更新 Win32 RDSHServer 物件的字串屬性值 \_ 。
ms.assetid: 9a338872-27fc-4e37-afd6-20a42c7859e5
ms.tgt_platform: multiple
keywords:
- SetStringProperty 方法遠端桌面服務
- SetStringProperty 方法遠端桌面服務，Win32_RDSHServer 類別
- Win32_RDSHServer 類別遠端桌面服務，SetStringProperty 方法
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d30812c0df943175f96c8ae43a4fe094725c74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104598"
---
# <a name="setstringproperty-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="1058a-106">Win32 RDSHServer 類別的 SetStringProperty 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1058a-106">SetStringProperty method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="1058a-107">更新 [**Win32 \_ RDSHServer**](win32-rdshserver.md) 物件的字串屬性值。</span><span class="sxs-lookup"><span data-stu-id="1058a-107">Updates a string property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1058a-108">語法</span><span class="sxs-lookup"><span data-stu-id="1058a-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="1058a-109">參數</span><span class="sxs-lookup"><span data-stu-id="1058a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1058a-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1058a-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1058a-111">識別要更新之屬性的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1058a-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="1058a-112">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1058a-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1058a-113">新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="1058a-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1058a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1058a-114">Return value</span></span>

<span data-ttu-id="1058a-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1058a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1058a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1058a-116">Requirements</span></span>



| <span data-ttu-id="1058a-117">需求</span><span class="sxs-lookup"><span data-stu-id="1058a-117">Requirement</span></span> | <span data-ttu-id="1058a-118">值</span><span class="sxs-lookup"><span data-stu-id="1058a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1058a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1058a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1058a-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="1058a-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1058a-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1058a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1058a-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1058a-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1058a-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="1058a-123">Namespace</span></span><br/>                | <span data-ttu-id="1058a-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="1058a-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1058a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1058a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1058a-126"><dt>Certenroll。h</dt></span><span class="sxs-lookup"><span data-stu-id="1058a-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="1058a-127">MOF</span><span class="sxs-lookup"><span data-stu-id="1058a-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1058a-128"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="1058a-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1058a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1058a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1058a-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1058a-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1058a-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1058a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1058a-132">**Win32 \_ RDSHServer**</span><span class="sxs-lookup"><span data-stu-id="1058a-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





