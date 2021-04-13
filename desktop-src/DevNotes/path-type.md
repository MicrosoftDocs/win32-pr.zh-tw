---
description: 表示當做引數使用的路徑類型。
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: PATH_TYPE 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510399"
---
# <a name="path_type-enumeration"></a><span data-ttu-id="e9b29-103">路徑 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="e9b29-103">PATH\_TYPE enumeration</span></span>

<span data-ttu-id="e9b29-104">表示當做引數使用的路徑類型。</span><span class="sxs-lookup"><span data-stu-id="e9b29-104">Represents the type of path being used as an argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b29-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9b29-105">Syntax</span></span>


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="e9b29-106">常數</span><span class="sxs-lookup"><span data-stu-id="e9b29-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e9b29-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**DOS \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="e9b29-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**DOS\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="e9b29-108">標準路徑。</span><span class="sxs-lookup"><span data-stu-id="e9b29-108">Standard path.</span></span>

</dd> <dt>

<span data-ttu-id="e9b29-109"><span id="NT_PATH"></span><span id="nt_path"></span>**NT \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="e9b29-109"><span id="NT_PATH"></span><span id="nt_path"></span>**NT\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="e9b29-110">內部路徑。</span><span class="sxs-lookup"><span data-stu-id="e9b29-110">Internal path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9b29-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9b29-111">Requirements</span></span>



| <span data-ttu-id="e9b29-112">需求</span><span class="sxs-lookup"><span data-stu-id="e9b29-112">Requirement</span></span> | <span data-ttu-id="e9b29-113">值</span><span class="sxs-lookup"><span data-stu-id="e9b29-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e9b29-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9b29-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e9b29-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9b29-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e9b29-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9b29-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e9b29-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9b29-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9b29-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9b29-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b29-119">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="e9b29-119">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> <dt>

[<span data-ttu-id="e9b29-120">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="e9b29-120">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




