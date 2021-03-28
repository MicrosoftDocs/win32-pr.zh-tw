---
description: 通知您已發生變更。
title: 'SMC_SHCHANGENOTIFY 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8232f170-0dab-475a-ace0-67c04f01c777
api_name:
- SMC_SHCHANGENOTIFY
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 258a885ddaf61b45df1cfff9f9c77ce37a233dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973273"
---
# <a name="smc_shchangenotify-message"></a><span data-ttu-id="8e94f-103">SMC \_ SHCHANGENOTIFY 訊息</span><span class="sxs-lookup"><span data-stu-id="8e94f-103">SMC\_SHCHANGENOTIFY message</span></span>

<span data-ttu-id="8e94f-104">通知您已發生變更。</span><span class="sxs-lookup"><span data-stu-id="8e94f-104">Notifies you that a change has taken place.</span></span>


```C++
SMC_SHCHANGENOTIFY
    lParam = (LPARAM) (PSMCSCHANGENOTIFYSTRUCT) psmc
            
```



## <a name="parameters"></a><span data-ttu-id="8e94f-105">參數</span><span class="sxs-lookup"><span data-stu-id="8e94f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e94f-106">*psmc*</span><span class="sxs-lookup"><span data-stu-id="8e94f-106">*psmc*</span></span> 
</dt> <dd>

<span data-ttu-id="8e94f-107">[**SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct)結構的指標，其中包含有關變更的資訊。</span><span class="sxs-lookup"><span data-stu-id="8e94f-107">A pointer to an [**SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) structure with information on the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e94f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e94f-108">Return value</span></span>

<span data-ttu-id="8e94f-109">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="8e94f-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e94f-110">備註</span><span class="sxs-lookup"><span data-stu-id="8e94f-110">Remarks</span></span>

<span data-ttu-id="8e94f-111">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="8e94f-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e94f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e94f-112">Requirements</span></span>



| <span data-ttu-id="8e94f-113">需求</span><span class="sxs-lookup"><span data-stu-id="8e94f-113">Requirement</span></span> | <span data-ttu-id="8e94f-114">值</span><span class="sxs-lookup"><span data-stu-id="8e94f-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e94f-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e94f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8e94f-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e94f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8e94f-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e94f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8e94f-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e94f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8e94f-119">標頭</span><span class="sxs-lookup"><span data-stu-id="8e94f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e94f-120"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="8e94f-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e94f-121">Idl</span><span class="sxs-lookup"><span data-stu-id="8e94f-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8e94f-122"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8e94f-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




