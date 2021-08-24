---
UID: ''
title: GuardCheckLongJumpTarget 函式
description: 嘗試驗證 longjmp 的目標是否有效。
old-location: ''
ms.assetid: na
ms.date: 04/02/2019
ms.keywords: ''
ms.topic: reference
req.header: guardapiset.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- api-ms-win-core-guard-l1-1-0.dll
api_name:
- GuardCheckLongJumpTarget
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: bcc8565401e09e8a4a3e0dfb221f240255b00bd0e91b9c2611b21db3ee1c0201
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002258"
---
# <a name="guardchecklongjumptarget-function"></a>GuardCheckLongJumpTarget 函式

## <a name="description"></a>描述

嘗試確認[longjmp](/cpp/c-runtime-library/reference/longjmp)的目標是否適用于已啟用[Control Flow Guard (CFG) ](../secbp/control-flow-guard.md)的進程。

如果目標位址對應至影像對應，就會針對二進位檔解壓縮有效的目標。
函數會使用這些目標來驗證目標。
如果二進位檔沒有描述有效 *longjmp* 目標集合的中繼資料，則函數會傳回 **TRUE**。

如果目標位址對應到非影像對應（如同在 JIT 程式碼中），則會參考全域唯讀原則來判斷是否允許跳躍。

## <a name="parameters"></a>參數

### <a name="targetaddress-in"></a>TargetAddress [in]

跳躍的目標位址。

### <a name="flags-in"></a>旗標 [in]

描述要在位址上執行之作業的旗標。
如果您指定 **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1) ，則如果目標無效，此函數不會終止進程。

## <a name="returns"></a>傳回

如果目標有效則 **為 TRUE** ，否則為 **FALSE**。

## <a name="remarks"></a>備註

## <a name="see-also"></a>另請參閱
