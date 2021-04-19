---
description: 從系統亂數產生器取出指定的隨機位元組數目。
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: SystemPrng 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966701"
---
# <a name="systemprng-function"></a>SystemPrng 函式

\[**SystemPrng** 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用 [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom)。\]

**SystemPrng** 函式會從系統亂數產生器取出指定的隨機位元組數目。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫此函數，您必須建立使用者定義的標頭檔。

 

## <a name="syntax"></a>語法


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbRandomData* \[擴展\]
</dt> <dd>

接收已抓取位元組之緩衝區的指標。

</dd> <dt>

*cbRandomData* \[在\]
</dt> <dd>

要擷取的位元組數。

</dd> </dl>

## <a name="return-value"></a>傳回值

一律傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows Vista （含 SP1） \[ 桌面應用程式\]<br/>                                                                                                                                                                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                                                                                                                                                           |
| DLL<br/>                      | <dl> <dt>Windows Server 2008 和 Windows Vista （含 SP1）上的Ksecdd.sys;</dt><dt>Windows 7 和 Windows Server 2008 R2 上的Cng.sys</dt> </dl> |



 

 




