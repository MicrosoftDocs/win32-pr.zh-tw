---
title: IConfigAsfWriter SetIndexMode 方法
description: SetIndexMode 方法可讓應用程式控制是否要將檔案暫時為索引。
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- SetIndexMode 方法 windows Media 格式
- SetIndexMode 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，SetIndexMode 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25d5f2b985aeca490323aecaef2595d52b99056c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023522"
---
# <a name="iconfigasfwritersetindexmode-method"></a>IConfigAsfWriter：： SetIndexMode 方法

**SetIndexMode** 方法可讓應用程式控制是否要將檔案暫時為索引。

## <a name="syntax"></a>語法


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bIndexFile* \[在\]
</dt> <dd>

**BOOL** 類型的變數;**TRUE** 指定將暫時索引的檔案。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，則會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

根據預設， [WM ASF 寫入器](wm-asf-writer-filter.md) 會建立暫時索引的 asf 檔案。 當圖形停止時，它會執行索引編制。 如果您想要做為後置處理步驟來執行您自己的框架型索引，則可以停用此行為。 若要建立框架索引檔案，請 (FALSE) 呼叫 **SetIndexMode** 、建立檔案，然後直接使用 Windows MEDIA 格式 SDK 方法來建立檔案的框架型索引。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 