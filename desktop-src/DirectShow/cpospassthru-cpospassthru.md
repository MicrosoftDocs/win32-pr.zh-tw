---
description: CPosPassThru。 CPosPassThru 函式-函數方法。
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: CPosPassThru. CPosPassThru 函數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a6c49b305b3c6638aeaaee1480d0b561fd8c99a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085596"
---
# <a name="cpospassthrucpospassthru-constructor"></a>CPosPassThru. CPosPassThru 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

物件名稱的指標，用於偵測用途。 在靜態記憶體中配置此參數。

</dd> <dt>

*朋 克* 
</dt> <dd>

這個物件之擁有者的指標。 如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。 否則，請將此參數設定為 **Null**。

</dd> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。 忽略。

</dd> <dt>

*pPin* 
</dt> <dd>

篩選器輸入釘選的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



