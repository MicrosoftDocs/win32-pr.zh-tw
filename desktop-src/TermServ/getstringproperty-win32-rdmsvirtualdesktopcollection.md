---
title: Win32_RDMSVirtualDesktopCollection 類別的 GetStringProperty 方法
description: 從虛擬桌面集合抓取字串屬性。
ms.assetid: 4a122fc5-1635-4d74-a90d-2347c0714fc7
ms.tgt_platform: multiple
keywords:
- GetStringProperty 方法遠端桌面服務
- GetStringProperty 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，GetStringProperty 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242d973d7ec8d320ed589933567b337a035f0e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999600"
---
# <a name="getstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="37b60-106">Win32 RDMSVirtualDesktopCollection 類別的 GetStringProperty 方法 \_</span><span class="sxs-lookup"><span data-stu-id="37b60-106">GetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="37b60-107">從虛擬桌面集合抓取字串屬性。</span><span class="sxs-lookup"><span data-stu-id="37b60-107">Retrieves a string property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="37b60-108">語法</span><span class="sxs-lookup"><span data-stu-id="37b60-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="37b60-109">參數</span><span class="sxs-lookup"><span data-stu-id="37b60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b60-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37b60-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37b60-111">識別要取得之屬性的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="37b60-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="37b60-112">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="37b60-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37b60-113">接收已抓取值的字串。</span><span class="sxs-lookup"><span data-stu-id="37b60-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b60-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="37b60-114">Return value</span></span>

<span data-ttu-id="37b60-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="37b60-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="37b60-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="37b60-116">Requirements</span></span>



| <span data-ttu-id="37b60-117">需求</span><span class="sxs-lookup"><span data-stu-id="37b60-117">Requirement</span></span> | <span data-ttu-id="37b60-118">值</span><span class="sxs-lookup"><span data-stu-id="37b60-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="37b60-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37b60-119">Minimum supported client</span></span><br/> | <span data-ttu-id="37b60-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="37b60-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="37b60-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37b60-121">Minimum supported server</span></span><br/> | <span data-ttu-id="37b60-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37b60-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="37b60-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="37b60-123">Namespace</span></span><br/>                | <span data-ttu-id="37b60-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="37b60-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="37b60-125">MOF</span><span class="sxs-lookup"><span data-stu-id="37b60-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37b60-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="37b60-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="37b60-127">DLL</span><span class="sxs-lookup"><span data-stu-id="37b60-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37b60-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37b60-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="37b60-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37b60-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b60-130">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="37b60-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





