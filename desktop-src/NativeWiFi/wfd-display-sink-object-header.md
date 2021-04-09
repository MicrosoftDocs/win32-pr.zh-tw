---
description: 描述通知或通知結果中所包含的顯示接收物件資料。
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: 'WFD_DISPLAY_SINK_OBJECT_HEADER 結構 (Wfdsink .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849136"
---
# <a name="wfd_display_sink_object_header-structure"></a><span data-ttu-id="e03ac-103">WFD \_ 顯示 \_ 接收 \_ 物件 \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="e03ac-103">WFD\_DISPLAY\_SINK\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="e03ac-104">[ **WFD \_ 顯示 \_ 接收 \_ 物件 \_ 標頭** ] 結構描述通知或通知結果中所包含的顯示接收物件資料。</span><span class="sxs-lookup"><span data-stu-id="e03ac-104">The **WFD\_DISPLAY\_SINK\_OBJECT\_HEADER** structure describes the display sink object data included in a notification or notification result.</span></span>

## <a name="syntax"></a><span data-ttu-id="e03ac-105">語法</span><span class="sxs-lookup"><span data-stu-id="e03ac-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="e03ac-106">成員</span><span class="sxs-lookup"><span data-stu-id="e03ac-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e03ac-107">**型別**</span><span class="sxs-lookup"><span data-stu-id="e03ac-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="e03ac-108">顯示接收物件的型別。</span><span class="sxs-lookup"><span data-stu-id="e03ac-108">The type of the display sink object.</span></span> <span data-ttu-id="e03ac-109">您可以使用識別碼 **WFD \_ 顯示 \_ 接收 \_ 物件 \_ 類型 \_ 預設** 值，其定義為值1。</span><span class="sxs-lookup"><span data-stu-id="e03ac-109">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_TYPE\_DEFAULT** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="e03ac-110">**修訂**</span><span class="sxs-lookup"><span data-stu-id="e03ac-110">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="e03ac-111">顯示接收物件的修訂版本。</span><span class="sxs-lookup"><span data-stu-id="e03ac-111">The revision version of the display sink object.</span></span> <span data-ttu-id="e03ac-112">您可以使用識別碼 **WFD \_ 顯示 \_ 接收 \_ 物件 \_ 修訂 \_ \_ 第1版** ，其定義為值1。</span><span class="sxs-lookup"><span data-stu-id="e03ac-112">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_REVISION\_VERSION\_1** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="e03ac-113">**長度**</span><span class="sxs-lookup"><span data-stu-id="e03ac-113">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="e03ac-114">通知或通知結果中的資料長度。</span><span class="sxs-lookup"><span data-stu-id="e03ac-114">The length of the data in the notification or notification result.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e03ac-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e03ac-115">Requirements</span></span>



| <span data-ttu-id="e03ac-116">需求</span><span class="sxs-lookup"><span data-stu-id="e03ac-116">Requirement</span></span> | <span data-ttu-id="e03ac-117">值</span><span class="sxs-lookup"><span data-stu-id="e03ac-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e03ac-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e03ac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e03ac-119">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e03ac-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e03ac-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e03ac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e03ac-121">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e03ac-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e03ac-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e03ac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e03ac-123"><dt>Wfdsink。h</dt></span><span class="sxs-lookup"><span data-stu-id="e03ac-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




