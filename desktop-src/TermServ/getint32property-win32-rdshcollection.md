---
title: 'Win32_RDSHCollection 類別的 GetInt32Property 方法 (appanalysis .h) '
description: 抓取 Win32 RDSHCollection 物件的整數屬性值 \_ 。
ms.assetid: ab68f357-057d-4a36-ae39-f47198768a49
ms.tgt_platform: multiple
keywords:
- GetInt32Property 方法遠端桌面服務
- GetInt32Property 方法遠端桌面服務，Win32_RDSHCollection 類別
- Win32_RDSHCollection 類別遠端桌面服務，GetInt32Property 方法
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5cc29234fe3bb1b92e68e728423931da965391f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685634"
---
# <a name="getint32property-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="94bba-106">Win32 RDSHCollection 類別的 GetInt32Property 方法 \_</span><span class="sxs-lookup"><span data-stu-id="94bba-106">GetInt32Property method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="94bba-107">抓取 [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) 物件的整數屬性值。</span><span class="sxs-lookup"><span data-stu-id="94bba-107">Retrieves an integer property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="94bba-108">語法</span><span class="sxs-lookup"><span data-stu-id="94bba-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="94bba-109">參數</span><span class="sxs-lookup"><span data-stu-id="94bba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94bba-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="94bba-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94bba-111">識別要取得之屬性的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="94bba-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="94bba-112">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="94bba-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94bba-113">接收已抓取的屬性值。</span><span class="sxs-lookup"><span data-stu-id="94bba-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94bba-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="94bba-114">Return value</span></span>

<span data-ttu-id="94bba-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="94bba-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="94bba-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="94bba-116">Requirements</span></span>



| <span data-ttu-id="94bba-117">需求</span><span class="sxs-lookup"><span data-stu-id="94bba-117">Requirement</span></span> | <span data-ttu-id="94bba-118">值</span><span class="sxs-lookup"><span data-stu-id="94bba-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94bba-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94bba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="94bba-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="94bba-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="94bba-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94bba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="94bba-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="94bba-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="94bba-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="94bba-123">Namespace</span></span><br/>                | <span data-ttu-id="94bba-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="94bba-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="94bba-125">標頭</span><span class="sxs-lookup"><span data-stu-id="94bba-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="94bba-126"><dt>Appanalysis。h</dt></span><span class="sxs-lookup"><span data-stu-id="94bba-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="94bba-127">MOF</span><span class="sxs-lookup"><span data-stu-id="94bba-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94bba-128"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="94bba-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="94bba-129">DLL</span><span class="sxs-lookup"><span data-stu-id="94bba-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94bba-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94bba-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="94bba-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94bba-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94bba-132">**Win32 \_ RDSHCollection**</span><span class="sxs-lookup"><span data-stu-id="94bba-132">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





