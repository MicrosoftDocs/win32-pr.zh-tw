---
description: GetMaximumCursors 方法會抓取 tablet 裝置支援的最大資料指標數目。
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: ITablet3：： GetMaximumCursors 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976960"
---
# <a name="itablet3getmaximumcursors-method"></a>ITablet3：： GetMaximumCursors 方法

**GetMaximumCursors** 方法會抓取 tablet 裝置支援的最大資料指標數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMaximumCursors* 
</dt> <dd>

裝置支援的輸入數目上限。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_成功時傳回 S OK，否則傳回錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> </dl>

 

 




