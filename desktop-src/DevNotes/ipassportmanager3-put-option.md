---
description: 設定特定的 Microsoft .NET Passport 登入選項。
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: IPassportManager3：:p ut_Option 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92a1c432df3f3948a85205e26da64073722ba84dd365ebdcaccf3b80521c517c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827188"
---
# <a name="ipassportmanager3put_option-method"></a>IPassportManager3：:p 的 \_ 選項方法

設定特定的 Microsoft .NET Passport 登入選項。

> [!Note]  
> **Put \_ 選項** 方法屬於 [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10))介面。 本主題補充最初的檔。

 

## <a name="syntax"></a>語法


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*name* 
</dt> <dd>

要設定的登入選項。 目前唯一支援的選項為 iMode。

</dd> <dt>

*newVal* 
</dt> <dd>

 ( VT \_ BOOL) 的 VARIANT，可指定選項的新值。 這個值可以是 True 或 False。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_當方法成功時傳回 S OK。

## <a name="remarks"></a>備註

此方法隨附于較舊版本的 Passport SDK。

 

 
