---
title: IConfigAsfWriter2 GetParam 方法
description: GetParam 方法會抓取指定之篩選準則設定參數的目前值。
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- GetParam 方法 windows Media 格式
- GetParam 方法 windows Media Format，IConfigAsfWriter2 介面
- IConfigAsfWriter2 介面 windows Media Format，GetParam 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a411e4b1896174e25a1f671f3f42fd83c1376713f10e9e4cb2b2d2186b3d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809138"
---
# <a name="iconfigasfwriter2getparam-method"></a>IConfigAsfWriter2：： GetParam 方法

**GetParam** 方法會抓取指定之篩選準則設定參數的目前值。

## <a name="syntax"></a>語法


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwParam* \[在\]
</dt> <dd>

指定要取出的參數。 它必須是[ \_ AM \_ ASFWRITERCONFIG \_ PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))列舉中所定義的值。

</dd> <dt>

*pdwParam1* \[擴展\]
</dt> <dd>

變數的指標，該變數會抓取 *dwParam* 中指定之參數的值。

</dd> <dt>

*pdwParam2* \[擴展\]
</dt> <dd>

未使用，必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，則會傳回 **HRESULT** 錯誤碼。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter2 介面**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2：： SetParam**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 