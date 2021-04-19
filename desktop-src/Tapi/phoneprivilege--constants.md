---
description: PHONEPRIVILEGE \_ 位旗標常數描述可開啟手機裝置的各種方式。
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: 'PHONEPRIVILEGE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995110"
---
# <a name="phoneprivilege_-constants"></a>PHONEPRIVILEGE \_ 常數

**PHONEPRIVILEGE \_** 位旗標常數描述可開啟手機裝置的各種方式。

<dl> <dt>

<span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**PHONEPRIVILEGE \_ 監視**
</dt> <dd> <dl> <dt>



使用 [監視] 許可權開啟手機裝置的應用程式，會收到關於電話上發生的事件和狀態變更的通知。 應用程式無法在手機裝置上叫用會變更其狀態的任何作業，因此只能叫用狀態作業。 多個應用程式可以在任何指定時間監視電話裝置。


</dt> </dl> </dd> <dt>

<span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PHONEPRIVILEGE \_ 擁有者**
</dt> <dd> <dl> <dt>



使用「擁有者」許可權開啟手機裝置的應用程式，可以變更手機的燈、響鈴、顯示、hookswitch 和資料區塊的狀態。 在 [擁有者] 模式中開啟手機裝置也會提供電話裝置的監視。 在任何指定的時間，都只允許一個應用程式成為電話裝置的擁有者。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




