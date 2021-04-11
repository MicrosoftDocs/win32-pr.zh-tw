---
description: 結構，用來識別要評估的主機和來源檔案。
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: 'WLDP_HOST_INFORMATION 結構 (Wldp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025829"
---
# <a name="wldp_host_information-structure"></a><span data-ttu-id="6733b-103">WLDP \_ 主機 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="6733b-103">WLDP\_HOST\_INFORMATION structure</span></span>

<span data-ttu-id="6733b-104">結構，用來識別要評估的主機和來源檔案。</span><span class="sxs-lookup"><span data-stu-id="6733b-104">A structure identifying the host and source file to be evaluated.</span></span>

## <a name="syntax"></a><span data-ttu-id="6733b-105">語法</span><span class="sxs-lookup"><span data-stu-id="6733b-105">Syntax</span></span>


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="6733b-106">成員</span><span class="sxs-lookup"><span data-stu-id="6733b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6733b-107">**dwRevision**</span><span class="sxs-lookup"><span data-stu-id="6733b-107">**dwRevision**</span></span>
</dt> <dd>

<span data-ttu-id="6733b-108">必須是 **WLDP \_ 主機 \_ 資訊 \_ 修訂**。</span><span class="sxs-lookup"><span data-stu-id="6733b-108">Must be **WLDP\_HOST\_INFORMATION\_REVISION**.</span></span>

</dd> <dt>

<span data-ttu-id="6733b-109">**dwHostId**</span><span class="sxs-lookup"><span data-stu-id="6733b-109">**dwHostId**</span></span>
</dt> <dd>

<span data-ttu-id="6733b-110">[**WLDP \_ 主機 \_ 識別碼**](wldp-host-id.md)中的列舉值，其描述主機識別碼。</span><span class="sxs-lookup"><span data-stu-id="6733b-110">Enumeration value from [**WLDP\_HOST\_ID**](wldp-host-id.md) that describes the host ID.</span></span>

</dd> <dt>

<span data-ttu-id="6733b-111">**szSource**</span><span class="sxs-lookup"><span data-stu-id="6733b-111">**szSource**</span></span>
</dt> <dd>

<span data-ttu-id="6733b-112">副檔名為的完整路徑和腳本名稱。</span><span class="sxs-lookup"><span data-stu-id="6733b-112">Full path and script name with the extension.</span></span> <span data-ttu-id="6733b-113">若為 **WLDP \_ 主機 \_ 識別碼 \_ 全域** 或手動腳本執行，則為 Null。</span><span class="sxs-lookup"><span data-stu-id="6733b-113">NULL for **WLDP\_HOST\_ID\_GLOBAL**, or manual script execution.</span></span>

</dd> <dt>

<span data-ttu-id="6733b-114">**hSource**</span><span class="sxs-lookup"><span data-stu-id="6733b-114">**hSource**</span></span>
</dt> <dd>

<span data-ttu-id="6733b-115">除了名稱之外，呼叫端還可以指定用於驗證之檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6733b-115">In addition to the name, the caller can specify a handle to the file used for validation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6733b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6733b-116">Requirements</span></span>



| <span data-ttu-id="6733b-117">需求</span><span class="sxs-lookup"><span data-stu-id="6733b-117">Requirement</span></span> | <span data-ttu-id="6733b-118">值</span><span class="sxs-lookup"><span data-stu-id="6733b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6733b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6733b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6733b-120">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6733b-120">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6733b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6733b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6733b-122">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6733b-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6733b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6733b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6733b-124"><dt>Wldp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6733b-124"><dt>Wldp.h</dt></span></span> </dl> |



 

 




