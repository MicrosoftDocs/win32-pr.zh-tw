---
description: 取得非同步動作完成時所呼叫的方法。
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: IAsyncAction：： get_Completed 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: bc018912b2b4643cc4ef2f48cc76eb997a2627fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113124"
---
# <a name="iasyncactionget_completed-method"></a><span data-ttu-id="23cca-103">IAsyncAction：： get \_ Completed 方法</span><span class="sxs-lookup"><span data-stu-id="23cca-103">IAsyncAction::get\_Completed method</span></span>

<span data-ttu-id="23cca-104">取得非同步動作完成時所呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="23cca-104">Gets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="23cca-105">語法</span><span class="sxs-lookup"><span data-stu-id="23cca-105">Syntax</span></span>


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a><span data-ttu-id="23cca-106">參數</span><span class="sxs-lookup"><span data-stu-id="23cca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23cca-107">*處理常式* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="23cca-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23cca-108">類型： **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="23cca-108">Type: **[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***</span></span>

<span data-ttu-id="23cca-109">處理完成通知的方法。</span><span class="sxs-lookup"><span data-stu-id="23cca-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23cca-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="23cca-110">Return value</span></span>

<span data-ttu-id="23cca-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="23cca-111">Type: **HRESULT**</span></span>

<span data-ttu-id="23cca-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="23cca-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="23cca-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="23cca-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="23cca-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="23cca-114">Requirements</span></span>



| <span data-ttu-id="23cca-115">需求</span><span class="sxs-lookup"><span data-stu-id="23cca-115">Requirement</span></span> | <span data-ttu-id="23cca-116">值</span><span class="sxs-lookup"><span data-stu-id="23cca-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23cca-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23cca-117">Minimum supported client</span></span><br/> | <span data-ttu-id="23cca-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="23cca-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="23cca-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23cca-119">Minimum supported server</span></span><br/> | <span data-ttu-id="23cca-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="23cca-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="23cca-121">標頭</span><span class="sxs-lookup"><span data-stu-id="23cca-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="23cca-122"><dt>Windows .idl</dt></span><span class="sxs-lookup"><span data-stu-id="23cca-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23cca-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23cca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23cca-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="23cca-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
