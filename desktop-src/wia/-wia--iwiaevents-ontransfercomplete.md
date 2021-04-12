---
description: 成功完成資料傳輸時所發生的事件。
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Wia. OnTransferComplete 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192803"
---
# <a name="wiaontransfercomplete-event"></a><span data-ttu-id="6ec9e-103">Wia. OnTransferComplete 事件</span><span class="sxs-lookup"><span data-stu-id="6ec9e-103">Wia.OnTransferComplete event</span></span>

<span data-ttu-id="6ec9e-104">成功完成資料傳輸時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="6ec9e-104">Event that occurs when a data transfer is completed successfully.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ec9e-105">Syntax</span></span>


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="6ec9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ec9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec9e-107">*Item*</span><span class="sxs-lookup"><span data-stu-id="6ec9e-107">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec9e-108">已傳送的 [**專案**](-wia-item.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="6ec9e-108">The [**Item**](-wia-item.md) object transferred.</span></span>

</dd> <dt>

<span data-ttu-id="6ec9e-109">*路徑*</span><span class="sxs-lookup"><span data-stu-id="6ec9e-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec9e-110">已傳送影像的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="6ec9e-110">The path and file name of the transferred image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec9e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ec9e-111">Return value</span></span>

<span data-ttu-id="6ec9e-112">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6ec9e-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec9e-113">備註</span><span class="sxs-lookup"><span data-stu-id="6ec9e-113">Remarks</span></span>

<span data-ttu-id="6ec9e-114">當資料傳輸、影像或音效順利完成時，WIA 會通知腳本或應用程式。</span><span class="sxs-lookup"><span data-stu-id="6ec9e-114">WIA notifies the script or application when a data transfer, image or sound, completes successfully.</span></span> <span data-ttu-id="6ec9e-115">執行 **objWia** \_ **OnTransferComplete ()** 副程式，以允許您的腳本或應用程式回應資料傳輸的完成。</span><span class="sxs-lookup"><span data-stu-id="6ec9e-115">Implement the **objWia**\_**OnTransferComplete()** subroutine to allow your script or application to respond to the completion of the data transfer.</span></span>

<span data-ttu-id="6ec9e-116">例如，您可能想要讓腳本在傳輸之後顯示影像。</span><span class="sxs-lookup"><span data-stu-id="6ec9e-116">For example, you might want a script to display an image after it is transferred.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec9e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ec9e-117">Requirements</span></span>



| <span data-ttu-id="6ec9e-118">需求</span><span class="sxs-lookup"><span data-stu-id="6ec9e-118">Requirement</span></span> | <span data-ttu-id="6ec9e-119">值</span><span class="sxs-lookup"><span data-stu-id="6ec9e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec9e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ec9e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec9e-121">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ec9e-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ec9e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ec9e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec9e-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ec9e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6ec9e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6ec9e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ec9e-125"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="6ec9e-125"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




