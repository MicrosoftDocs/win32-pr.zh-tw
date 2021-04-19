---
description: 提供 IPStore 介面的 COM 標準列舉方法。
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: 'IEnumPStoreProviders 介面 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e01bd28722fdb4d5a0ff7e3db4f715ddc1df2315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996036"
---
# <a name="ienumpstoreproviders-interface"></a>IEnumPStoreProviders 介面

\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

提供 [**IPStore**](ipstore.md) 介面的 COM 標準列舉方法。

## <a name="members"></a>成員

**IEnumPStoreProviders** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IEnumPStoreProviders** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IEnumPStoreProviders** 介面具有這些方法。



| 方法                                      | 描述                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**克隆**](ienumpstoreproviders-clone.md) | 建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。<br/> |
| [**下一步**](ienumpstoreproviders-next.md)   | 取得列舉順序中的下一個指定提供者。<br/>                           |
| [**重設**](ienumpstoreproviders-reset.md) | 重設為列舉序列的開頭。<br/>                                    |
| [**跳過**](ienumpstoreproviders-skip.md)   | 略過列舉序列中指定的提供者。<br/>                               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
