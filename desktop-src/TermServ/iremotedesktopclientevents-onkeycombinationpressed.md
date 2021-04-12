---
title: IRemoteDesktopClientEvents OnKeyCombinationPressed 方法
description: 在遠端會話中按下特殊按鍵組合時呼叫。
ms.assetid: 0A4EAD6C-5DA9-4ED3-BA79-92AE5AE81C9F
ms.tgt_platform: multiple
keywords:
- OnKeyCombinationPressed 方法遠端桌面服務
- OnKeyCombinationPressed 方法遠端桌面服務，IRemoteDesktopClientEvents 介面
- IRemoteDesktopClientEvents 介面遠端桌面服務，OnKeyCombinationPressed 方法
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnKeyCombinationPressed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192cad6323578a9bde9fe38af1d2b1d2cf83473c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384290"
---
# <a name="iremotedesktopclienteventsonkeycombinationpressed-method"></a><span data-ttu-id="29be0-106">IRemoteDesktopClientEvents：： OnKeyCombinationPressed 方法</span><span class="sxs-lookup"><span data-stu-id="29be0-106">IRemoteDesktopClientEvents::OnKeyCombinationPressed method</span></span>

<span data-ttu-id="29be0-107">在遠端會話中按下特殊按鍵組合時呼叫。</span><span class="sxs-lookup"><span data-stu-id="29be0-107">Called when special key combinations are pressed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="29be0-108">語法</span><span class="sxs-lookup"><span data-stu-id="29be0-108">Syntax</span></span>


```C++
void OnKeyCombinationPressed(
  [in] long keyCombination
);
```



## <a name="parameters"></a><span data-ttu-id="29be0-109">參數</span><span class="sxs-lookup"><span data-stu-id="29be0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29be0-110">*keyCombination* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29be0-110">*keyCombination* \[in\]</span></span>
<span data-ttu-id="29be0-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="29be0-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="29be0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="29be0-112">Return value</span></span>

<span data-ttu-id="29be0-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="29be0-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="29be0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="29be0-114">Requirements</span></span>



| <span data-ttu-id="29be0-115">需求</span><span class="sxs-lookup"><span data-stu-id="29be0-115">Requirement</span></span> | <span data-ttu-id="29be0-116">值</span><span class="sxs-lookup"><span data-stu-id="29be0-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29be0-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29be0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="29be0-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="29be0-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="29be0-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29be0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="29be0-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29be0-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="29be0-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="29be0-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="29be0-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29be0-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="29be0-123">DLL</span><span class="sxs-lookup"><span data-stu-id="29be0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29be0-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29be0-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="29be0-125">IID</span><span class="sxs-lookup"><span data-stu-id="29be0-125">IID</span></span><br/>                      | <span data-ttu-id="29be0-126">DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="29be0-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29be0-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29be0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29be0-128">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="29be0-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





