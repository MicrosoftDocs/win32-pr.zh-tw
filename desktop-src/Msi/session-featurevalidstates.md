---
description: Session 物件的 FeatureValidStates 屬性會傳回代表位旗標的整數，其中每個相關位代表指定功能的有效安裝狀態。
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: FeatureValidStates 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991134"
---
# <a name="sessionfeaturevalidstates-property"></a>FeatureValidStates 屬性

[**Session**](session-object.md)物件的 **FeatureValidStates** 屬性會傳回代表位旗標的整數，其中每個相關位代表指定功能的有效安裝狀態。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a>屬性值

要抓取其有效安裝狀態的功能專案所需的字串名稱。

## <a name="remarks"></a>備註

傳回值是由位旗標所組成，如下所示。 位0：如果設定，則本機是有效的狀態。 位1：如果設定，則來源是有效的狀態。

只有在安裝程式呼叫 [CostInitialize](costinitialize-action.md)和 [CostFinalize](costfinalize-action.md)動作之後， **FeatureValidStates** 屬性才會成功。

**FeatureValidStates** 會藉由查詢連結至指定功能的所有元件，而不考慮任何元件目前已安裝的狀態，來決定狀態有效性。

功能可能有效的狀態如下所示：

-   如果功能不包含元件，則 INSTALLSTATE \_ 本機和 INSTALLSTATE \_ 來源都是功能的有效狀態。
-   如果功能的至少一個元件具有 msidbComponentAttributesLocalOnly 或 msidbComponentAttributesOptional 的屬性，則 INSTALLSTATE \_ LOCAL 會是此功能的有效狀態。
-   如果功能的至少一個元件具有 msidbComponentAttributesSourceOnly 或 msidbComponentAttributesOptional 的屬性，則 INSTALLSTATE \_ 來源會是此功能的有效狀態。
-   如果屬於功能的元件檔案已修補或從壓縮的來源進行修補，則 INSTALLSTATE \_ 來源不會包含為功能的有效狀態。
-   \_如果功能不允許公告 (msidbFeatureAttributesDisallowAdvertise) 或功能需要 (msidbFeatureAttributesNoUnsupportedAdvertise) 的平臺支援，而且平臺不支援它，則 INSTALLSTATE 公告不是有效的狀態。
-   \_如果功能的屬性不包含 msidbFeatureAttributesUIDisallowAbsent，則 INSTALLSTATE 不會是此功能的有效狀態。
-   標示為遵循父功能的子功能的有效狀態 (msidbFeatureAttributesFollowParent) 是根據父功能的動作或已安裝的狀態。

如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




