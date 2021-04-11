---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: 'D (WMI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d469b94ec6649c64722fb414880d2e79fc3c88b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026854"
---
# <a name="d-wmi"></a>D (WMI) 

[B](gloss-a.md) [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**Datetime**
</dt> <dd>

請參閱 [*CIM datetime*](gloss-c.md)。

</dd> <dt>

<span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**低耦合提供者**
</dt> <dd>

裝載在與 WMI 不同的處理序中的提供者。 由於提供者可以控制其本身的存留期，而不是每次使用者透過 WMI 存取提供者時啟動，因此建議使用低耦合提供者來檢測應用程式。

</dd> <dt>

<span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**直接存取**
</dt> <dd>

在腳本中存取 WMI 提供的屬性和方法，就像是 [**SWbemObject**](swbemobject.md)的 automation 屬性和方法一樣。

Nondirect 存取： `VolumeName = MyDisk.Properties_("VolumeName")`

直接存取： `VolumeName = MyDisk.VolumeName`

</dd> <dt>

<span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**分散式管理工作強制 (DMTF)**
</dt> <dd>

適用于重要技術廠商（包括 Microsoft）的國際標準組織，可領導開發、採用和統一桌面、企業和網際網路環境的管理標準和計畫。

</dd> <dt>

<span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**
</dt> <dd>

請參閱 *分散式管理工作強制 (DMTF)*。

</dd> <dt>

<span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**動態類別**
</dt> <dd>

CIM 類別，其定義是由 [*提供者*](gloss-p.md) 在執行時間依需要提供。 動態類別代表提供者特定的 [*managed 物件*](gloss-m.md) ，而且不會儲存在 [*CIM 存放庫*](gloss-c.md)中。 動態類別僅支援 *動態實例*。

</dd> <dt>

<span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**動態實例**
</dt> <dd>

當需要時， [*提供者*](gloss-p.md) 所提供之 CIM 類別的實例。 它不會儲存在 [*CIM 存放庫*](gloss-c.md)中。 可以為靜態或動態類別提供動態實例。 動態支援類別的實例可讓提供者提供最新的 [*屬性*](gloss-p.md) 值。

</dd> </dl>

 

 



