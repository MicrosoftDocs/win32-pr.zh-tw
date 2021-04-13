---
description: 抓取特定 Microsoft .NET Passport 登入選項的值。
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: IPassportManager3：： get_Option 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385860"
---
# <a name="ipassportmanager3get_option-method"></a>IPassportManager3：： get \_ 選項方法

抓取特定 Microsoft .NET Passport 登入選項的值。

> [!Note]  
> **Get \_ 選項** 方法屬於 [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10))介面。 本主題補充最初的檔。

 

## <a name="syntax"></a>語法


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

要取出的登入選項。 目前唯一支援的選項是 "iMode"。

</dd> <dt>

*pVal* \[擴展\]
</dt> <dd>

**變數** 的指標， (VT \_ BOOL) ，可接收選項的值。 這個值可以是 True 或 False。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_當方法成功時傳回 S OK。

## <a name="remarks"></a>備註

此方法隨附于較舊版本的 Passport SDK。

 

 
