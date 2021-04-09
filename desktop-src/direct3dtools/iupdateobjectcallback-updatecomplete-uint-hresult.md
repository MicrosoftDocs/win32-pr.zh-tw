---
description: 回呼，用來通知主機物件已更新。
MS-HAID: vspixengine.IUpdateObjectCallback\_UpdateComplete\_UINT\_HRESULT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IUpdateObjectCallback：： UpdateComplete 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7F54DDEC-E595-4615-B9B7-B1213A58B362
api_name:
- IUpdateObjectCallback.UpdateComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b601d8ac785f65c4400821741b83e76bd6987481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109297"
---
# <a name="span-idvspixengineiupdateobjectcallback_updatecomplete_uint_hresultspaniupdateobjectcallbackupdatecomplete-method"></a><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>IUpdateObjectCallback：： UpdateComplete 方法

回呼，用來通知主機物件已更新。

## <a name="syntax"></a>語法


```C++
HRESULT UpdateComplete(
   UINT    objectAddress,
   HRESULT result
);
```

## <a name="parameters"></a>參數

*objectAddress*   
已更新之物件的識別碼。

*結果*   
指出更新是否成功。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IUpdateObjectCallback**](/windows/desktop/direct3dtools/iupdateobjectcallback)

 

 
