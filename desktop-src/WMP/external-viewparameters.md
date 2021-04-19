---
title: ViewParameters
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |ViewParameters
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- ViewParameters Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0adec580a68bd3f6b92beef1de814729848179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995940"
---
# <a name="externalviewparameters"></a>ViewParameters

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**ViewParameters** 屬性會在 Windows Media Player 中，抓取與目前視圖相關聯的參數。

## <a name="syntax"></a>Syntax

**viewParameters**

## <a name="possible-values"></a>可能的值

這個屬性會傳回唯讀 **字串**。

## <a name="remarks"></a>備註

這個屬性會抓取線上商店先前設定的參數。 例如，線上商店可以在 [changeView](external-changeview.md)方法的 *ViewParams* 參數或 [changeViewOnlineList](external-changeviewonlinelist.md)方法的 *Params* 參數中指定 view 參數。

Windows Media Player 不會解讀 View 參數。 它們是由線上商店所建立，而且只有線上商店才有意義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





