---
title: IConfigAsfWriter SetIndexMode 方法
description: SetIndexMode 方法可讓應用程式控制是否要將檔案暫時為索引。
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- SetIndexMode 方法 windows Media 格式
- SetIndexMode 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，SetIndexMode 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25d5f2b985aeca490323aecaef2595d52b99056c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023522"
---
# <a name="iconfigasfwritersetindexmode-method"></a><span data-ttu-id="de578-106">IConfigAsfWriter：： SetIndexMode 方法</span><span class="sxs-lookup"><span data-stu-id="de578-106">IConfigAsfWriter::SetIndexMode method</span></span>

<span data-ttu-id="de578-107">**SetIndexMode** 方法可讓應用程式控制是否要將檔案暫時為索引。</span><span class="sxs-lookup"><span data-stu-id="de578-107">The **SetIndexMode** method enables the application to control whether the file will be temporally indexed.</span></span>

## <a name="syntax"></a><span data-ttu-id="de578-108">語法</span><span class="sxs-lookup"><span data-stu-id="de578-108">Syntax</span></span>


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="de578-109">參數</span><span class="sxs-lookup"><span data-stu-id="de578-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de578-110">*bIndexFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de578-110">*bIndexFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de578-111">**BOOL** 類型的變數;**TRUE** 指定將暫時索引的檔案。</span><span class="sxs-lookup"><span data-stu-id="de578-111">Variable of type **BOOL**; **TRUE** specifies that the file will be temporally indexed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de578-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="de578-112">Return value</span></span>

<span data-ttu-id="de578-113">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="de578-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="de578-114">如果失敗，則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="de578-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de578-115">備註</span><span class="sxs-lookup"><span data-stu-id="de578-115">Remarks</span></span>

<span data-ttu-id="de578-116">根據預設， [WM ASF 寫入器](wm-asf-writer-filter.md) 會建立暫時索引的 asf 檔案。</span><span class="sxs-lookup"><span data-stu-id="de578-116">By default, the [WM ASF Writer](wm-asf-writer-filter.md) creates temporally indexed ASF files.</span></span> <span data-ttu-id="de578-117">當圖形停止時，它會執行索引編制。</span><span class="sxs-lookup"><span data-stu-id="de578-117">It performs the indexing when the graph stops.</span></span> <span data-ttu-id="de578-118">如果您想要做為後置處理步驟來執行您自己的框架型索引，則可以停用此行為。</span><span class="sxs-lookup"><span data-stu-id="de578-118">You can disable this behavior if you want to do your own frame-based indexing as a post-processing step.</span></span> <span data-ttu-id="de578-119">若要建立框架索引檔案，請 (FALSE) 呼叫 **SetIndexMode** 、建立檔案，然後直接使用 Windows MEDIA 格式 SDK 方法來建立檔案的框架型索引。</span><span class="sxs-lookup"><span data-stu-id="de578-119">To create a frame-indexed file, call **SetIndexMode**(FALSE), create the file, and then use the Windows Media Format SDK methods directly to create a frame-based index for the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="de578-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de578-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="de578-121">[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="de578-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 