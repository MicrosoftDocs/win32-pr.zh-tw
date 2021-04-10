---
title: 'MPCOMPONENT_VERSION 結構 (MpClient .h) '
description: 個別元件的版本和更新時間。
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION 結構舊版 Windows 環境功能
- PMPCOMPONENT_VERSION 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934322"
---
# <a name="mpcomponent_version-structure"></a><span data-ttu-id="96c14-105">MPCOMPONENT \_ 版本結構</span><span class="sxs-lookup"><span data-stu-id="96c14-105">MPCOMPONENT\_VERSION structure</span></span>

<span data-ttu-id="96c14-106">個別元件的版本和更新時間。</span><span class="sxs-lookup"><span data-stu-id="96c14-106">Version and update time for an individual component.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c14-107">語法</span><span class="sxs-lookup"><span data-stu-id="96c14-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a><span data-ttu-id="96c14-108">成員</span><span class="sxs-lookup"><span data-stu-id="96c14-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="96c14-109">**版本**</span><span class="sxs-lookup"><span data-stu-id="96c14-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="96c14-110">類型： **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="96c14-110">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="96c14-111">版本欄位。</span><span class="sxs-lookup"><span data-stu-id="96c14-111">Version field.</span></span> <span data-ttu-id="96c14-112">每個 **單字** 都代表主要、次要、組建和修訂。</span><span class="sxs-lookup"><span data-stu-id="96c14-112">Each **WORD** represents major, minor, build, and revision.</span></span>

</dd> <dt>

<span data-ttu-id="96c14-113">**UpdateTime**</span><span class="sxs-lookup"><span data-stu-id="96c14-113">**UpdateTime**</span></span>
</dt> <dd>

<span data-ttu-id="96c14-114">類型： **ULARGE \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="96c14-114">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="96c14-115">元件的上次更新時間（以 **FILETIME** 格式）。</span><span class="sxs-lookup"><span data-stu-id="96c14-115">Last update time of the component, in **FILETIME** format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96c14-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="96c14-116">Requirements</span></span>



| <span data-ttu-id="96c14-117">需求</span><span class="sxs-lookup"><span data-stu-id="96c14-117">Requirement</span></span> | <span data-ttu-id="96c14-118">值</span><span class="sxs-lookup"><span data-stu-id="96c14-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96c14-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96c14-119">Minimum supported client</span></span><br/> | <span data-ttu-id="96c14-120">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96c14-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="96c14-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96c14-121">Minimum supported server</span></span><br/> | <span data-ttu-id="96c14-122">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96c14-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96c14-123">標頭</span><span class="sxs-lookup"><span data-stu-id="96c14-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="96c14-124"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="96c14-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





