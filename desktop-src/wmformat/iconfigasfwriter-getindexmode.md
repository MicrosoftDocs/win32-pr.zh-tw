---
title: IConfigAsfWriter GetIndexMode 方法
description: GetIndexMode 方法會抓取目前的時態性索引模式。
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- GetIndexMode 方法 windows Media 格式
- GetIndexMode 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，GetIndexMode 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375825"
---
# <a name="iconfigasfwritergetindexmode-method"></a>IConfigAsfWriter：： GetIndexMode 方法

**GetIndexMode** 方法會抓取目前的時態性索引模式。

## <a name="syntax"></a>語法


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbIndexFile* \[擴展\]
</dt> <dd>

**BOOL** 類型變數的指標，此變數會接收時態性索引模式設定。 **TRUE** 值表示已將 WM ASF 寫入器設定為寫入暫時的索引檔案。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，則會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

使用這個方法來判斷是否目前將 [WM ASF 寫入器](wm-asf-writer-filter.md) 設定為寫入暫時索引的 asf 檔案。 如需暫時索引和框架索引檔案的詳細資訊，請參閱 [**IConfigAsfWriter：： SetIndexMode**](iconfigasfwriter-setindexmode.md)的備註。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 