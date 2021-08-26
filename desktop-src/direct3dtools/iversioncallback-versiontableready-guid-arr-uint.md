---
description: 回呼函式，用來通知主機支援的介面。
MS-HAID: vspixengine.IVersionCallback\_VersionTableReady\_GUID\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IVersionCallback：： VersionTableReady 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 58D5E6B4-2CF8-4C13-9A62-93418D46CBCF
api_name:
- IVersionCallback.VersionTableReady
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 680a9db6fe72dcf11dc6ecb13cf64fede9cf375e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626534"
---
# <a name="span-idvspixengineiversioncallback_versiontableready_guid_arr_uintspaniversioncallbackversiontableready-method"></a><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback：： VersionTableReady 方法

回呼函式，用來通知主機支援的介面。

## <a name="syntax"></a>語法


```C++
HRESULT VersionTableReady(
   GUID [] count1_interfaceIds,
   UINT    count
);
```

## <a name="parameters"></a>參數

*count1 \_ interfaceIds*   
陣列，其中包含支援之介面識別碼的 Guid。

*計數*   
傳遞至 count1 interfaceIds 的 Guid 數目 \_ 。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IVersionCallback**](/windows/desktop/direct3dtools/iversioncallback)

 

 
