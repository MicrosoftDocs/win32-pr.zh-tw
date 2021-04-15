---
description: 釋出材質，並以非同步方式通知主機。
MS-HAID: vspixengine.IPixEngine5\_FreeTextureAsync\_UINT\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5：： FreeTextureAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A2D46D4-AA09-4E50-8109-774CE7F538E7
api_name:
- IPixEngine5.FreeTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aed7d29653b9da6f39b1ef6ec4e600c1857744f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467905"
---
# <a name="span-idvspixengineipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dwordspanipixengine5freetextureasync-method"></a><span id="vspixengine.ipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5：： FreeTextureAsync 方法

釋出材質，並以非同步方式通知主機。

## <a name="syntax"></a>語法


```C++
HRESULT FreeTextureAsync(
   UINT                  textureId,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a>參數

*textureId*   
要釋放之材質的識別碼。

*回檔*   
提供 IPixEngine5 回呼介面之物件的位址。

*requestCookie*   
可唯一 idenfies 要求的 cookie，而且可用來指示它被取消。

*progressIntervalMsecs*   
未使用。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
