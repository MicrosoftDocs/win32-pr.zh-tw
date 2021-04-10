---
description: GetSPRM 方法會抓取指定的系統參數 register。
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: GetSPRM 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935630"
---
# <a name="getsprm-method"></a>GetSPRM 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

方法會抓取 `GetSPRM` 指定的系統參數暫存器。

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

指定您想要取出其值作為整數的註冊。 整數的範圍必須介於0到23之間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回整數值，代表指定之暫存器的內容。

## <a name="remarks"></a>備註

光碟控制項系統參數會註冊 (SPRMs) 。 播放機應用程式不需要存取這些暫存器，即可取得任何標準導覽功能。 SPRMs 代表播放程式的狀態。 每一個都有意義，由使用者喜好設定、光碟命令，以及應用程式無法直接控制的其他專案來設定。 應用程式可以讀取這些暫存器，但無法寫入這些暫存器。 若要有效地使用這些暫存器，您可能需要更深入瞭解 DVD 流覽命令，而非本檔所提供的資訊。 下表顯示每個註冊的內容。 如需註冊內容的詳細資訊，請參閱 [ **IDvdInfo2：： GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)



| 註冊 | 目錄                        |
|----------|---------------------------------|
| 0        | 功能表語言代碼              |
| 1        | 音訊串流號碼             |
| 2        | 子圖片資料流程號碼        |
| 3        | 目前的角度數位            |
| 4        | 目前的標題編號            |
| 5        | 標題編號                    |
| 6        | PGC 編號                      |
| 7        | 目前的章節號碼 (PLATFORM PTT)     |
| 8        | 反白顯示的按鈕編號       |
| 9        | 流覽計時器                |
| 10       | Nav 的 PGC 跳躍。 計時器         |
| 11       | 卡拉卡拉音訊簡報模式 |
| 12       | >PROCMONTRACE.PML 國家/地區碼         |
| 13       | Pml                             |
| 14       | 影片設定                   |
| 15       | 音訊功能                |
| 16       | 音訊語言                  |
| 17       | 音訊語言延伸模組        |
| 18       | 子圖片語言             |
| 19       | 子圖片語言延伸模組   |
| 20       | 播放程式區功能變數代碼              |
| 21       | 保留                        |
| 22       | 保留                        |
| 23       | 保留                        |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetGPRM**](getgprm-method.md)
</dt> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



