---
title: GestureAt 方法
description: GestureAt 方法
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462988"
---
# <a name="gestureat-method"></a><span data-ttu-id="e9dc2-103">GestureAt 方法</span><span class="sxs-lookup"><span data-stu-id="e9dc2-103">GestureAt Method</span></span>

<span data-ttu-id="e9dc2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e9dc2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e9dc2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="e9dc2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e9dc2-106">在指定的位置播放指定字元的 gesturing 動畫。</span><span class="sxs-lookup"><span data-stu-id="e9dc2-106">Plays the gesturing animation for the specified character at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="e9dc2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="e9dc2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e9dc2-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。GestureAt* \*  *x、y*</span><span class="sxs-lookup"><span data-stu-id="e9dc2-108">*agent ***.Characters ("*** CharacterID\*\*\*").GestureAt*\* *x,y*</span></span>



| <span data-ttu-id="e9dc2-109">部分</span><span class="sxs-lookup"><span data-stu-id="e9dc2-109">Part</span></span>  | <span data-ttu-id="e9dc2-110">描述</span><span class="sxs-lookup"><span data-stu-id="e9dc2-110">Description</span></span>                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9dc2-111">*x、y*</span><span class="sxs-lookup"><span data-stu-id="e9dc2-111">*x,y*</span></span> | <span data-ttu-id="e9dc2-112">必要。</span><span class="sxs-lookup"><span data-stu-id="e9dc2-112">Required.</span></span> <span data-ttu-id="e9dc2-113">整數值，指出字元將手勢的水準 (*x*) 螢幕座標和垂直 (*y*) 螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="e9dc2-113">An integer value that indicates the horizontal (*x*) screen coordinate and vertical (*y*) screen coordinate to which the character will gesture.</span></span> <span data-ttu-id="e9dc2-114">這些座標必須以圖元為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="e9dc2-114">These coordinates must be specified in pixels.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9dc2-115">備註</span><span class="sxs-lookup"><span data-stu-id="e9dc2-115">Remarks</span></span>

<span data-ttu-id="e9dc2-116">伺服器會自動播放適當的動畫以朝指定的位置進行手勢。</span><span class="sxs-lookup"><span data-stu-id="e9dc2-116">The server automatically plays the appropriate animation to gesture toward the specified location.</span></span> <span data-ttu-id="e9dc2-117">座標一律相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="e9dc2-117">The coordinates are always relative to the screen origin (upper left).</span></span>

<span data-ttu-id="e9dc2-118">如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="e9dc2-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="e9dc2-119">此外，如果尚未在本機電腦上載入相關聯的動畫，伺服器會將 **要求** 物件的 [ [**狀態**](status-property.md) ] 屬性設定為 [失敗]，並提供適當的錯誤號碼。</span><span class="sxs-lookup"><span data-stu-id="e9dc2-119">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="e9dc2-120">因此，如果您使用 HTTP 通訊協定來存取字元動畫資料，請在呼叫 **GestureAt** 方法之前，使用 [**Get**](get-method.md)方法載入 **Gesturing** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="e9dc2-120">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Gesturing** state animations before calling the **GestureAt** method.</span></span>

 

 