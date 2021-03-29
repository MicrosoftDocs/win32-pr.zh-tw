---
description: 通知您新的專案，如隨附的 SMDATA 結構所指定。
title: 'SMC_NEWITEM 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e0ccf2db-cb46-469f-bc08-4b5100a410ba
api_name:
- SMC_NEWITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ebd8f1b6454a2fb592374b860811ebfc7a14f09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973452"
---
# <a name="smc_newitem-message"></a><span data-ttu-id="32dbc-103">SMC \_ NEWITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="32dbc-103">SMC\_NEWITEM message</span></span>

<span data-ttu-id="32dbc-104">通知您新的專案，如隨附的 [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) 結構所指定。</span><span class="sxs-lookup"><span data-stu-id="32dbc-104">Notifies you of a new item, as specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_NEWITEM
            
```



## <a name="parameters"></a><span data-ttu-id="32dbc-105">參數</span><span class="sxs-lookup"><span data-stu-id="32dbc-105">Parameters</span></span>

<span data-ttu-id="32dbc-106">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="32dbc-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32dbc-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="32dbc-107">Return value</span></span>

<span data-ttu-id="32dbc-108">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="32dbc-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="32dbc-109">備註</span><span class="sxs-lookup"><span data-stu-id="32dbc-109">Remarks</span></span>

<span data-ttu-id="32dbc-110">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="32dbc-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="32dbc-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="32dbc-111">Requirements</span></span>



| <span data-ttu-id="32dbc-112">需求</span><span class="sxs-lookup"><span data-stu-id="32dbc-112">Requirement</span></span> | <span data-ttu-id="32dbc-113">值</span><span class="sxs-lookup"><span data-stu-id="32dbc-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32dbc-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32dbc-114">Minimum supported client</span></span><br/> | <span data-ttu-id="32dbc-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32dbc-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="32dbc-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32dbc-116">Minimum supported server</span></span><br/> | <span data-ttu-id="32dbc-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32dbc-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="32dbc-118">標頭</span><span class="sxs-lookup"><span data-stu-id="32dbc-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="32dbc-119"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="32dbc-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="32dbc-120">Idl</span><span class="sxs-lookup"><span data-stu-id="32dbc-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32dbc-121"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="32dbc-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




