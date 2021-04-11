---
description: Item 物件的 TakePicture 方法會讓數位相機裝置拍攝圖片，並傳回代表所產生影像的專案物件。 此方法僅適用于數位相機裝置。
ms.assetid: d181048e-21ef-4fcc-a50a-5ba44bbde72e
title: 'TakePicture 方法 (Wiavideo .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.TakePicture
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: fd07f7ccd4f2c65c2d911dabdd0ca829dc241765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944315"
---
# <a name="itemtakepicture-method"></a><span data-ttu-id="37d42-104">TakePicture 方法</span><span class="sxs-lookup"><span data-stu-id="37d42-104">Item.TakePicture method</span></span>

<span data-ttu-id="37d42-105">[**Item**](-wia-item.md)物件的 **TakePicture** 方法會讓數位相機裝置拍攝圖片，並傳回代表所產生影像的 **專案** 物件。</span><span class="sxs-lookup"><span data-stu-id="37d42-105">The **TakePicture** method of the [**Item**](-wia-item.md) object causes a digital camera device to take a picture and returns an **Item** object that represents the resulting image.</span></span> <span data-ttu-id="37d42-106">此方法僅適用于數位相機裝置。</span><span class="sxs-lookup"><span data-stu-id="37d42-106">This method applies only to digital camera devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="37d42-107">語法</span><span class="sxs-lookup"><span data-stu-id="37d42-107">Syntax</span></span>


```JScript
retVal = Item.TakePicture()
```



## <a name="parameters"></a><span data-ttu-id="37d42-108">參數</span><span class="sxs-lookup"><span data-stu-id="37d42-108">Parameters</span></span>

<span data-ttu-id="37d42-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="37d42-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37d42-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="37d42-110">Return value</span></span>

<span data-ttu-id="37d42-111">類型： **IWiaDispatchItem**</span><span class="sxs-lookup"><span data-stu-id="37d42-111">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="37d42-112">代表這個方法所建立之影像的 [**專案**](-wia-item.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="37d42-112">An [**Item**](-wia-item.md) object that represents the image that this method creates.</span></span>

## <a name="requirements"></a><span data-ttu-id="37d42-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="37d42-113">Requirements</span></span>



| <span data-ttu-id="37d42-114">需求</span><span class="sxs-lookup"><span data-stu-id="37d42-114">Requirement</span></span> | <span data-ttu-id="37d42-115">值</span><span class="sxs-lookup"><span data-stu-id="37d42-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37d42-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37d42-116">Minimum supported client</span></span><br/> | <span data-ttu-id="37d42-117">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37d42-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37d42-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37d42-118">Minimum supported server</span></span><br/> | <span data-ttu-id="37d42-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37d42-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="37d42-120">標頭</span><span class="sxs-lookup"><span data-stu-id="37d42-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="37d42-121"><dt>Wiavideo。h</dt></span><span class="sxs-lookup"><span data-stu-id="37d42-121"><dt>Wiavideo.h</dt></span></span> </dl>                         |
| <span data-ttu-id="37d42-122">DLL</span><span class="sxs-lookup"><span data-stu-id="37d42-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37d42-123"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="37d42-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




