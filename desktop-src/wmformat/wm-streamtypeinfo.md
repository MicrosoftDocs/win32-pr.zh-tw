---
title: WM/StreamTypeInfo
description: WM/StreamTypeInfo 屬性包含 ASF 檔案中指定之資料流程的設定資訊。
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- WM/StreamTypeInfo windows Media 格式
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104372942"
---
# <a name="wmstreamtypeinfo"></a><span data-ttu-id="9c3bf-104">WM/StreamTypeInfo</span><span class="sxs-lookup"><span data-stu-id="9c3bf-104">WM/StreamTypeInfo</span></span>

<span data-ttu-id="9c3bf-105">**WM/StreamTypeInfo** 屬性包含 ASF 檔案中指定之資料流程的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="9c3bf-105">The **WM/StreamTypeInfo** attribute contains the configuration information for the specified stream in the ASF file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9c3bf-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="9c3bf-106">Global Constant</span></span>

<span data-ttu-id="9c3bf-107">g \_ wszWMStreamTypeInfo</span><span class="sxs-lookup"><span data-stu-id="9c3bf-107">g\_wszWMStreamTypeInfo</span></span>

## <a name="data-type"></a><span data-ttu-id="9c3bf-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="9c3bf-108">Data Type</span></span>

<span data-ttu-id="9c3bf-109">[**WM \_資料流程 \_ 類型 \_ 資訊**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT \_ 類型 \_ BINARY**) </span><span class="sxs-lookup"><span data-stu-id="9c3bf-109">[**WM\_STREAM\_TYPE\_INFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="9c3bf-110">備註</span><span class="sxs-lookup"><span data-stu-id="9c3bf-110">Remarks</span></span>

<span data-ttu-id="9c3bf-111">這個屬性會套用到特定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9c3bf-111">This attribute applies to specific streams.</span></span> <span data-ttu-id="9c3bf-112">您無法抓取資料流程0的這個屬性。</span><span class="sxs-lookup"><span data-stu-id="9c3bf-112">You cannot retrieve this attribute for stream 0.</span></span>

<span data-ttu-id="9c3bf-113">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9c3bf-113">This attribute is read-only.</span></span>

<span data-ttu-id="9c3bf-114">您可以使用 [中繼資料編輯器] 物件來存取 **WM/StreamTypeInfo** 。</span><span class="sxs-lookup"><span data-stu-id="9c3bf-114">**WM/StreamTypeInfo** can be accessed by the metadata editor object.</span></span> <span data-ttu-id="9c3bf-115">這是存取串流設定資訊的唯一方法，不需要使用 reader 物件 (或同步讀取器物件) 來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="9c3bf-115">This is the only way to access stream configuration information without opening the file with the reader object (or the synchronous reader object).</span></span>

## <a name="see-also"></a><span data-ttu-id="9c3bf-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c3bf-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c3bf-117">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="9c3bf-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




