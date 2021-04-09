---
description: 指出是否應該將內容訊息傳送至擁有視窗的視窗程式。
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: CONTEXT_ENABLE_TYPE 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: cd741eeff1cc3e2ce055a84dd646c3aa2563f217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694544"
---
# <a name="context_enable_type-enumeration"></a><span data-ttu-id="0cc63-103">內容 \_ 啟用 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="0cc63-103">CONTEXT\_ENABLE\_TYPE enumeration</span></span>

<span data-ttu-id="0cc63-104">指出是否應該將內容訊息傳送至擁有視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="0cc63-104">Indicates whether context messages should be sent to the owning window's window procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc63-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cc63-105">Syntax</span></span>


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="0cc63-106">常數</span><span class="sxs-lookup"><span data-stu-id="0cc63-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0cc63-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**\_啟用內容**</span><span class="sxs-lookup"><span data-stu-id="0cc63-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**CONTEXT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0cc63-108">應該啟用平板電腦內容，以產生將內容訊息傳送至擁有視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="0cc63-108">The tablet context should be enabled, resulting in context messages being sent to the owning window's window procedure.</span></span>

</dd> <dt>

<span data-ttu-id="0cc63-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**內容 \_ 停用**</span><span class="sxs-lookup"><span data-stu-id="0cc63-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**CONTEXT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0cc63-110">應該停用 tablet 內容，防止任何進一步的內容訊息傳送至主控視窗的視窗程式或事件接收器。</span><span class="sxs-lookup"><span data-stu-id="0cc63-110">The tablet context should be disabled, preventing any further context messages from being sent to the owning window's window procedure or event sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0cc63-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cc63-111">Requirements</span></span>



| <span data-ttu-id="0cc63-112">需求</span><span class="sxs-lookup"><span data-stu-id="0cc63-112">Requirement</span></span> | <span data-ttu-id="0cc63-113">值</span><span class="sxs-lookup"><span data-stu-id="0cc63-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0cc63-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0cc63-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0cc63-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cc63-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0cc63-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0cc63-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0cc63-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="0cc63-117">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="0cc63-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cc63-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc63-119">**ITablet：： CreateCoNtext 方法**</span><span class="sxs-lookup"><span data-stu-id="0cc63-119">**ITablet::CreateContext Method**</span></span>](itablet-createcontext.md)
</dt> </dl>

 

 




