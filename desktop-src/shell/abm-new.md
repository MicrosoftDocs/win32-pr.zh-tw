---
description: 註冊新的 appbar，並指定系統應該用來傳送通知訊息的訊息識別碼。 Appbar 應該會在傳送任何其他 appbar 訊息之前傳送此訊息。
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: 'ABM_NEW 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689832"
---
# <a name="abm_new-message"></a><span data-ttu-id="c46ab-104">ABM \_ 新訊息</span><span class="sxs-lookup"><span data-stu-id="c46ab-104">ABM\_NEW message</span></span>

<span data-ttu-id="c46ab-105">註冊新的 appbar，並指定系統應該用來傳送通知訊息的訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="c46ab-105">Registers a new appbar and specifies the message identifier that the system should use to send it notification messages.</span></span> <span data-ttu-id="c46ab-106">Appbar 應該會在傳送任何其他 appbar 訊息之前傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c46ab-106">An appbar should send this message before sending any other appbar messages.</span></span>


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="c46ab-107">參數</span><span class="sxs-lookup"><span data-stu-id="c46ab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c46ab-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="c46ab-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="c46ab-109">[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標，其中包含新 appbar 的視窗控制碼和訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="c46ab-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the new appbar's window handle and message identifier.</span></span> <span data-ttu-id="c46ab-110">傳送此訊息時，您必須指定 **cbSize**、 **hWnd** 和 **uCallbackMessage** 成員;所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c46ab-110">You must specify the **cbSize**, **hWnd**, and **uCallbackMessage** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c46ab-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c46ab-111">Return value</span></span>

<span data-ttu-id="c46ab-112">如果成功，則傳回 **TRUE** ; 如果發生錯誤或已註冊 appbar，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c46ab-112">Returns **TRUE** if successful, or **FALSE** if an error occurs or if the appbar is already registered.</span></span>

## <a name="requirements"></a><span data-ttu-id="c46ab-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c46ab-113">Requirements</span></span>



| <span data-ttu-id="c46ab-114">需求</span><span class="sxs-lookup"><span data-stu-id="c46ab-114">Requirement</span></span> | <span data-ttu-id="c46ab-115">值</span><span class="sxs-lookup"><span data-stu-id="c46ab-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c46ab-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c46ab-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c46ab-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c46ab-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c46ab-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c46ab-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c46ab-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c46ab-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c46ab-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c46ab-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c46ab-121"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c46ab-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




