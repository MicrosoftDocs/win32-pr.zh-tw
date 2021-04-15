---
description: 將圖形記錄檔儲存至指定的位置。
MS-HAID: vspixengine.IPixEngine\_SaveFile\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine：： SaveFile 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A80498F4-C8F5-4AC0-92C5-A90EB2A090B7
api_name:
- IPixEngine.SaveFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f7e1bed8765ca64123ccf13cbc3ee5f0d989b115
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510342"
---
# <a name="span-idvspixengineipixengine_savefile_bstr_ifileiocallback_ptrspanipixenginesavefile-method"></a><span data-ttu-id="9b5d5-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>IPixEngine：： SaveFile 方法</span><span class="sxs-lookup"><span data-stu-id="9b5d5-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>IPixEngine::SaveFile method</span></span>

<span data-ttu-id="9b5d5-104">將圖形記錄檔儲存至指定的位置。</span><span class="sxs-lookup"><span data-stu-id="9b5d5-104">Saves the graphics log to the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b5d5-105">語法</span><span class="sxs-lookup"><span data-stu-id="9b5d5-105">Syntax</span></span>


```C++
HRESULT SaveFile(
   BSTR             FileName,
   IFileIOCallback* pFileIOCallback
);
```

## <a name="parameters"></a><span data-ttu-id="9b5d5-106">參數</span><span class="sxs-lookup"><span data-stu-id="9b5d5-106">Parameters</span></span>

<span data-ttu-id="9b5d5-107">*檔案名* </span><span class="sxs-lookup"><span data-stu-id="9b5d5-107">*FileName* </span></span>  
<span data-ttu-id="9b5d5-108">COM 字串，其中包含已儲存之圖形記錄檔的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="9b5d5-108">A COM string containing the pathname of the saved graphics log.</span></span>

<span data-ttu-id="9b5d5-109">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="9b5d5-109">*pFileIOCallback* </span></span>  
<span data-ttu-id="9b5d5-110">函式的位址，用來在儲存期間通知主機檔案 IO 錯誤。</span><span class="sxs-lookup"><span data-stu-id="9b5d5-110">The address of a functon used to notify the host of file IO errors during save.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b5d5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b5d5-111">Return value</span></span>

<span data-ttu-id="9b5d5-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9b5d5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b5d5-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9b5d5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b5d5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b5d5-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9b5d5-115">標頭</span><span class="sxs-lookup"><span data-stu-id="9b5d5-115">Header</span></span></p></td><td><span data-ttu-id="9b5d5-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="9b5d5-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9b5d5-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b5d5-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9b5d5-118">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="9b5d5-118">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
