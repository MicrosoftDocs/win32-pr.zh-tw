---
description: IEnumPStoreTypes 介面-提供 IPStore 介面的 COM 標準列舉方法。
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: 'IEnumPStoreTypes 介面 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7ca2e250864889a5fda465e146287bf59a2b6346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089356"
---
# <a name="ienumpstoretypes-interface"></a>IEnumPStoreTypes 介面

\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

提供 [**IPStore**](ipstore.md) 介面的 COM 標準列舉方法。

## <a name="members"></a>成員

**IEnumPStoreTypes** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IEnumPStoreTypes** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IEnumPStoreTypes** 介面具有這些方法。



| 方法                                  | 描述                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**克隆**](ienumpstoretypes-clone.md) | 建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。<br/> |
| [**下一步**](ienumpstoretypes-next.md)   | 取得列舉順序中的下一個指定提供者類型。<br/>                      |
| [**重設**](ienumpstoretypes-reset.md) | 重設為列舉序列的開頭。<br/>                                    |
| [**跳過**](ienumpstoretypes-skip.md)   | 略過列舉序列中指定的提供者類型。<br/>                          |



 

## <a name="remarks"></a>備註

當列舉值物件不再使用時，必須釋放它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
