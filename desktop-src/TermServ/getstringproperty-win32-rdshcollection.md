---
title: Win32_RDSHCollection 類別的 GetStringProperty 方法
description: 抓取 Win32 RDSHCollection 物件的字串屬性值 \_ 。
ms.assetid: 8e97cd91-0e45-4d87-acfb-ee7d70376ce0
ms.tgt_platform: multiple
keywords:
- GetStringProperty 方法遠端桌面服務
- GetStringProperty 方法遠端桌面服務，Win32_RDSHCollection 類別
- Win32_RDSHCollection 類別遠端桌面服務，GetStringProperty 方法
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1895f05317850374a4f4b24d407a4c4ace9c5db7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934065"
---
# <a name="getstringproperty-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="40f50-106">Win32 RDSHCollection 類別的 GetStringProperty 方法 \_</span><span class="sxs-lookup"><span data-stu-id="40f50-106">GetStringProperty method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="40f50-107">抓取 [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) 物件的字串屬性值。</span><span class="sxs-lookup"><span data-stu-id="40f50-107">Retrieves a string property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="40f50-108">語法</span><span class="sxs-lookup"><span data-stu-id="40f50-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="40f50-109">參數</span><span class="sxs-lookup"><span data-stu-id="40f50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40f50-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40f50-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40f50-111">識別要取得之屬性的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="40f50-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="40f50-112">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="40f50-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40f50-113">接收已抓取的屬性值。</span><span class="sxs-lookup"><span data-stu-id="40f50-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40f50-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="40f50-114">Return value</span></span>

<span data-ttu-id="40f50-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="40f50-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="40f50-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="40f50-116">Requirements</span></span>



| <span data-ttu-id="40f50-117">需求</span><span class="sxs-lookup"><span data-stu-id="40f50-117">Requirement</span></span> | <span data-ttu-id="40f50-118">值</span><span class="sxs-lookup"><span data-stu-id="40f50-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="40f50-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40f50-119">Minimum supported client</span></span><br/> | <span data-ttu-id="40f50-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="40f50-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="40f50-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40f50-121">Minimum supported server</span></span><br/> | <span data-ttu-id="40f50-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="40f50-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="40f50-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="40f50-123">Namespace</span></span><br/>                | <span data-ttu-id="40f50-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="40f50-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="40f50-125">MOF</span><span class="sxs-lookup"><span data-stu-id="40f50-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40f50-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="40f50-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="40f50-127">DLL</span><span class="sxs-lookup"><span data-stu-id="40f50-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40f50-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40f50-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="40f50-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40f50-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f50-130">**Win32 \_ RDSHCollection**</span><span class="sxs-lookup"><span data-stu-id="40f50-130">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





