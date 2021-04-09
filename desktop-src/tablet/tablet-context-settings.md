---
description: 包含用來建立平板電腦內容的資訊。
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: TABLET_CONTEXT_SETTINGS 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945351"
---
# <a name="tablet_context_settings-structure"></a><span data-ttu-id="ef687-103">TABLET \_ 內容 \_ 設定結構</span><span class="sxs-lookup"><span data-stu-id="ef687-103">TABLET\_CONTEXT\_SETTINGS structure</span></span>

<span data-ttu-id="ef687-104">包含用來建立平板電腦內容的資訊。</span><span class="sxs-lookup"><span data-stu-id="ef687-104">Contains information used in creating a tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef687-105">語法</span><span class="sxs-lookup"><span data-stu-id="ef687-105">Syntax</span></span>


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a><span data-ttu-id="ef687-106">成員</span><span class="sxs-lookup"><span data-stu-id="ef687-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ef687-107">**cPktProps**</span><span class="sxs-lookup"><span data-stu-id="ef687-107">**cPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="ef687-108">封包中的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="ef687-108">The number of properties in a packet.</span></span>

</dd> <dt>

<span data-ttu-id="ef687-109">**pguidPktProps**</span><span class="sxs-lookup"><span data-stu-id="ef687-109">**pguidPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="ef687-110">封包屬性的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef687-110">Unique identifiers for the packet properties.</span></span>

</dd> <dt>

<span data-ttu-id="ef687-111">**cPktBtns**</span><span class="sxs-lookup"><span data-stu-id="ef687-111">**cPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="ef687-112">按鈕的數目。</span><span class="sxs-lookup"><span data-stu-id="ef687-112">The number of buttons.</span></span>

</dd> <dt>

<span data-ttu-id="ef687-113">**pguidPktBtns**</span><span class="sxs-lookup"><span data-stu-id="ef687-113">**pguidPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="ef687-114">按鈕的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef687-114">Unique identifiers for the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="ef687-115">**pdwBtnDnMask**</span><span class="sxs-lookup"><span data-stu-id="ef687-115">**pdwBtnDnMask**</span></span>
</dt> <dd>

<span data-ttu-id="ef687-116">按鈕下遮罩。</span><span class="sxs-lookup"><span data-stu-id="ef687-116">The button down mask.</span></span>

</dd> <dt>

<span data-ttu-id="ef687-117">**pdwBtnUpMask**</span><span class="sxs-lookup"><span data-stu-id="ef687-117">**pdwBtnUpMask**</span></span>
</dt> <dd>

<span data-ttu-id="ef687-118">按鈕的遮罩。</span><span class="sxs-lookup"><span data-stu-id="ef687-118">The button up mask.</span></span>

</dd> <dt>

<span data-ttu-id="ef687-119">**lXMargin**</span><span class="sxs-lookup"><span data-stu-id="ef687-119">**lXMargin**</span></span>
</dt> <dd>

<span data-ttu-id="ef687-120">X 方向邊界。</span><span class="sxs-lookup"><span data-stu-id="ef687-120">The X direction margin.</span></span>

</dd> <dt>

<span data-ttu-id="ef687-121">**lYMargin**</span><span class="sxs-lookup"><span data-stu-id="ef687-121">**lYMargin**</span></span>
</dt> <dd>

<span data-ttu-id="ef687-122">Y 方向邊界。</span><span class="sxs-lookup"><span data-stu-id="ef687-122">The Y direction margin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef687-123">備註</span><span class="sxs-lookup"><span data-stu-id="ef687-123">Remarks</span></span>

<span data-ttu-id="ef687-124">一般而言，應用程式會從 [**ITablet：： GetDefaultCoNtextSettings 方法**](itablet-getdefaultcontextsettings.md)取得預設值、修改值以符合其需求，然後將修改過的設定結構傳遞至 [**ITablet：： CreateCoNtext 方法**](itablet-createcontext.md)。</span><span class="sxs-lookup"><span data-stu-id="ef687-124">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the [**ITablet::CreateContext Method**](itablet-createcontext.md).</span></span>

<span data-ttu-id="ef687-125">此結構會決定應用程式將取得哪些事件、如何處理這些事件，以及如何將它們傳遞給應用程式或 Windows 本身。</span><span class="sxs-lookup"><span data-stu-id="ef687-125">This structure determines what events an application will get, how they will be processed, and how they will be delivered to the application or to Windows itself.</span></span>

<span data-ttu-id="ef687-126">按鈕會一起遮罩，以決定內容將處理哪些種類的事件。</span><span class="sxs-lookup"><span data-stu-id="ef687-126">The button masks together determine what kinds of events will be processed by the context.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef687-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef687-127">Requirements</span></span>



| <span data-ttu-id="ef687-128">需求</span><span class="sxs-lookup"><span data-stu-id="ef687-128">Requirement</span></span> | <span data-ttu-id="ef687-129">值</span><span class="sxs-lookup"><span data-stu-id="ef687-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ef687-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef687-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ef687-131">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef687-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ef687-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef687-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ef687-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="ef687-133">None supported</span></span><br/>                                     |



 

 




