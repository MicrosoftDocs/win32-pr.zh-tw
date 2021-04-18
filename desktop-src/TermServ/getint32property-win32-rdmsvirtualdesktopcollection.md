---
title: 'Win32_RDMSVirtualDesktopCollection 類別的 GetInt32Property 方法 (appanalysis .h) '
description: 從虛擬桌面集合抓取整數屬性。
ms.assetid: 18ffca65-e7c0-4b17-902f-d74b2a81aba2
ms.tgt_platform: multiple
keywords:
- GetInt32Property 方法遠端桌面服務
- GetInt32Property 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，GetInt32Property 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e8e5518590bece8e8b904ea56bf7572b436b66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968742"
---
# <a name="getint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="c8963-106">Win32 RDMSVirtualDesktopCollection 類別的 GetInt32Property 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c8963-106">GetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="c8963-107">從虛擬桌面集合抓取整數屬性。</span><span class="sxs-lookup"><span data-stu-id="c8963-107">Retrieves an integer property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8963-108">語法</span><span class="sxs-lookup"><span data-stu-id="c8963-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="c8963-109">參數</span><span class="sxs-lookup"><span data-stu-id="c8963-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8963-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8963-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8963-111">識別要取得之屬性的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c8963-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c8963-112">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c8963-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8963-113">接收已抓取值的整數。</span><span class="sxs-lookup"><span data-stu-id="c8963-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8963-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8963-114">Return value</span></span>

<span data-ttu-id="c8963-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c8963-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8963-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8963-116">Requirements</span></span>



| <span data-ttu-id="c8963-117">需求</span><span class="sxs-lookup"><span data-stu-id="c8963-117">Requirement</span></span> | <span data-ttu-id="c8963-118">值</span><span class="sxs-lookup"><span data-stu-id="c8963-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8963-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8963-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c8963-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="c8963-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="c8963-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8963-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c8963-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8963-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="c8963-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="c8963-123">Namespace</span></span><br/>                | <span data-ttu-id="c8963-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="c8963-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="c8963-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c8963-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8963-126"><dt>Appanalysis。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8963-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="c8963-127">MOF</span><span class="sxs-lookup"><span data-stu-id="c8963-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8963-128"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8963-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="c8963-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c8963-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8963-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8963-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="c8963-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8963-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8963-132">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="c8963-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





