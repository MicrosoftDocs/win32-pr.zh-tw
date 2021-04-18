---
description: 將 debug 符號路徑傳送至本機 (非遠端) 引擎的要求。
MS-HAID: vspixengine.ISymbolSettings\_UpdateSymbolSettings\_SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ISymbolSettings：： UpdateSymbolSettings 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E48E509F-8C33-49D6-B799-B16F70C1AA64
api_name:
- ISymbolSettings.UpdateSymbolSettings
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4c60ceacbf8d11f951896979862dad6520c32837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971276"
---
# <a name="span-idvspixengineisymbolsettings_updatesymbolsettings_symbolserverinfospanisymbolsettingsupdatesymbolsettings-method"></a><span data-ttu-id="a9254-103"><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>ISymbolSettings：： UpdateSymbolSettings 方法</span><span class="sxs-lookup"><span data-stu-id="a9254-103"><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>ISymbolSettings::UpdateSymbolSettings method</span></span>

<span data-ttu-id="a9254-104">將 debug 符號路徑傳送至本機 (非遠端) 引擎的要求。</span><span class="sxs-lookup"><span data-stu-id="a9254-104">A request to send debug symbol paths to the local (non-remote) engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9254-105">語法</span><span class="sxs-lookup"><span data-stu-id="a9254-105">Syntax</span></span>


```C++
HRESULT UpdateSymbolSettings(
   SymbolServerInfo symbolServerInfo
);
```

## <a name="parameters"></a><span data-ttu-id="a9254-106">參數</span><span class="sxs-lookup"><span data-stu-id="a9254-106">Parameters</span></span>

<span data-ttu-id="a9254-107">*symbolServerInfo* </span><span class="sxs-lookup"><span data-stu-id="a9254-107">*symbolServerInfo* </span></span>  
<span data-ttu-id="a9254-108">Debug 符號伺服器路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="a9254-108">Debug symbol server path information.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9254-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9254-109">Return value</span></span>

<span data-ttu-id="a9254-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a9254-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9254-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a9254-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9254-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9254-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a9254-113">標頭</span><span class="sxs-lookup"><span data-stu-id="a9254-113">Header</span></span></p></td><td><span data-ttu-id="a9254-114">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="a9254-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a9254-115"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9254-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a9254-116">**ISymbolSettings**</span><span class="sxs-lookup"><span data-stu-id="a9254-116">**ISymbolSettings**</span></span>](/windows/desktop/direct3dtools/isymbolsettings)

 

 
