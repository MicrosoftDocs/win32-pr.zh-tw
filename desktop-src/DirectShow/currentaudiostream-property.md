---
description: CurrentAudioStream 屬性會設定或抓取已啟用之音訊串流的數目。
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: CurrentAudioStream 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd814d5b560ed55ea312fbebb8678c67b1422b0cf3d47917fbf772f56a0d3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075968"
---
# <a name="currentaudiostream-property"></a>CurrentAudioStream 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`CurrentAudioStream`屬性會設定或抓取已啟用的音訊資料流程數目。

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a>傳回值

傳回從0到7的整數值，表示目前的音訊資料流程。

## <a name="remarks"></a>備註

此屬性是讀取/寫入，沒有預設值。 嘗試設定新的音訊串流之前，請先呼叫 [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) 來確認資料流程是否可用。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AudioStreamsAvailable**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



