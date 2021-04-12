---
title: Win32_VirtualDesktopSession 類別的 SendMessage 方法
description: 透過虛擬桌面會話傳送訊息給使用者。
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- SendMessage 方法遠端桌面服務
- SendMessage 方法遠端桌面服務，Win32_VirtualDesktopSession 類別
- Win32_VirtualDesktopSession 類別遠端桌面服務，SendMessage 方法
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e3e72f5c401b8cbb0e5e5de45f594d61af6275
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384573"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a><span data-ttu-id="84495-106">Win32 VirtualDesktopSession 類別的 SendMessage 方法 \_</span><span class="sxs-lookup"><span data-stu-id="84495-106">SendMessage method of the Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="84495-107">透過虛擬桌面會話傳送訊息給使用者。</span><span class="sxs-lookup"><span data-stu-id="84495-107">Send a message to the user through the virtual desktop session.</span></span>

## <a name="syntax"></a><span data-ttu-id="84495-108">語法</span><span class="sxs-lookup"><span data-stu-id="84495-108">Syntax</span></span>


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a><span data-ttu-id="84495-109">參數</span><span class="sxs-lookup"><span data-stu-id="84495-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84495-110">*標題* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84495-110">*Title* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84495-111">訊息的標題。</span><span class="sxs-lookup"><span data-stu-id="84495-111">The title of the messge.</span></span>

</dd> <dt>

<span data-ttu-id="84495-112">*訊息* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84495-112">*Message* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84495-113">訊息的內容。</span><span class="sxs-lookup"><span data-stu-id="84495-113">The content of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84495-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="84495-114">Return value</span></span>

<span data-ttu-id="84495-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="84495-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="84495-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="84495-116">Requirements</span></span>



| <span data-ttu-id="84495-117">需求</span><span class="sxs-lookup"><span data-stu-id="84495-117">Requirement</span></span> | <span data-ttu-id="84495-118">值</span><span class="sxs-lookup"><span data-stu-id="84495-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="84495-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84495-119">Minimum supported client</span></span><br/> | <span data-ttu-id="84495-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="84495-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="84495-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84495-121">Minimum supported server</span></span><br/> | <span data-ttu-id="84495-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84495-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="84495-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="84495-123">Namespace</span></span><br/>                | <span data-ttu-id="84495-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="84495-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="84495-125">MOF</span><span class="sxs-lookup"><span data-stu-id="84495-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84495-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="84495-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="84495-127">DLL</span><span class="sxs-lookup"><span data-stu-id="84495-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84495-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84495-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="84495-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84495-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84495-130">**Win32 \_ VirtualDesktopSession**</span><span class="sxs-lookup"><span data-stu-id="84495-130">**Win32\_VirtualDesktopSession**</span></span>](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





