---
description: 取得物件資料表支援哪些資料行 (物件資料) 類型的資訊。
MS-HAID: vspixengine.IObjectTableCallback\_GetSupportedColumns\_DWORD\_ObjectTableColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IObjectTableCallback：： GetSupportedColumns 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 148AB80D-9833-4B57-9F34-CEDFFF8E905A
api_name:
- IObjectTableCallback.GetSupportedColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ed077e0921043245e4ff3dda4b1c33dd4e3f20d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467580"
---
# <a name="span-idvspixengineiobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arrspaniobjecttablecallbackgetsupportedcolumns-method"></a><span data-ttu-id="a0be6-103"><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>IObjectTableCallback：： GetSupportedColumns 方法</span><span class="sxs-lookup"><span data-stu-id="a0be6-103"><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>IObjectTableCallback::GetSupportedColumns method</span></span>

<span data-ttu-id="a0be6-104">取得物件資料表支援哪些資料行 (物件資料) 類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="a0be6-104">Gets information about which columns (types of object data) are supported by the object table.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0be6-105">語法</span><span class="sxs-lookup"><span data-stu-id="a0be6-105">Syntax</span></span>


```C++
HRESULT GetSupportedColumns(
   DWORD                  numColumns,
   ObjectTableColumnID [] count0_pIDs,
   BSTR []                count0_pBstrNames
);
```

## <a name="parameters"></a><span data-ttu-id="a0be6-106">參數</span><span class="sxs-lookup"><span data-stu-id="a0be6-106">Parameters</span></span>

<span data-ttu-id="a0be6-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="a0be6-107">*numColumns* </span></span>  
<span data-ttu-id="a0be6-108">物件資料表支援的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="a0be6-108">The number of columns supported by the object table.</span></span>

<span data-ttu-id="a0be6-109">*count0_pIDs* </span><span class="sxs-lookup"><span data-stu-id="a0be6-109">*count0_pIDs* </span></span>  
<span data-ttu-id="a0be6-110">物件資料表所支援之每個資料行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0be6-110">The IDs of each column supported by the object table.</span></span>

<span data-ttu-id="a0be6-111">*count0_pBstrNames* </span><span class="sxs-lookup"><span data-stu-id="a0be6-111">*count0_pBstrNames* </span></span>  
<span data-ttu-id="a0be6-112">物件資料表所支援之每個資料行的名稱，做為 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="a0be6-112">The names of each column, as a COM string, supported by the object table.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0be6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0be6-113">Return value</span></span>

<span data-ttu-id="a0be6-114">如果這個方法成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="a0be6-114">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a0be6-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a0be6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0be6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0be6-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a0be6-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a0be6-117">Header</span></span></p></td><td><span data-ttu-id="a0be6-118">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="a0be6-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a0be6-119"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0be6-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a0be6-120">**IObjectTableCallback**</span><span class="sxs-lookup"><span data-stu-id="a0be6-120">**IObjectTableCallback**</span></span>](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
