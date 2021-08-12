---
description: 要求更新物件的初始狀態;例如紋理或著色器。
MS-HAID: vspixengine.IUpdateObject\_UpdateObject\_UINT\_DWORD\_BYTE\_arr\_IUpdateObjectCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IUpdateObject：： UpdateObject 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 824AB599-7377-4F77-8FC8-41E17ED57A79
api_name:
- IUpdateObject.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b48e206d09c784ac2f2df31eeab0d65cac04f740a66874fe9e436f96b8349143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282271"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject：： UpdateObject 方法

要求更新物件的初始狀態;例如紋理或著色器。

## <a name="syntax"></a>語法


```C++
HRESULT UpdateObject(
   UINT                    objectAddress,
   DWORD                   size,
   BYTE []                 count1_buffer,
   IUpdateObjectCallback * pCallback
);
```

## <a name="parameters"></a>參數

*objectAddress*   
要更新之物件的識別碼。

*大小*   
更新承載的大小（以位元組為單位）。

*count1 \_ 緩衝區*   
更新裝載。

*pCallback*   
用來通知主機物件已更新之函式的位址。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IUpdateObject**](/windows/desktop/direct3dtools/iupdateobject)

 

 
