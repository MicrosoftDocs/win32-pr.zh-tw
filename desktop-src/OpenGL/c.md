---
title: 'C (OpenGL) '
description: 以字母 C 為開頭之 OpenGL 詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- 用戶端電腦
- 用戶端記憶體
- 剪輯座標
- 裁剪
- 色彩索引
- 色彩索引模式
- 色彩對應
- components
- 內容
- 凸
- 凸殼
- 座標系統
- 撲殺
- 目前的矩陣
- 目前的點陣位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c9534052533745b1037aa80f26f435a163ee46
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024488"
---
# <a name="c-opengl"></a><span data-ttu-id="39aeb-118">C (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="39aeb-118">C (OpenGL)</span></span>

<span data-ttu-id="39aeb-119">[](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="39aeb-119">[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="39aeb-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**用戶端電腦**</span><span class="sxs-lookup"><span data-stu-id="39aeb-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**client computer**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-121">用來發出 OpenGL 命令的電腦。</span><span class="sxs-lookup"><span data-stu-id="39aeb-121">The computer from which OpenGL commands are issued.</span></span> <span data-ttu-id="39aeb-122">發出 OpenGL 命令的電腦可以透過網路連接到執行命令的另一部電腦，或者可以在同一部電腦上發出和執行命令。</span><span class="sxs-lookup"><span data-stu-id="39aeb-122">The computer that issues OpenGL commands can be connected through a network to a different computer that executes the commands, or commands can be issued and executed on the same computer.</span></span> <span data-ttu-id="39aeb-123">另請參閱 [伺服器](s.md)。</span><span class="sxs-lookup"><span data-stu-id="39aeb-123">See also [server](s.md).</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**用戶端記憶體**</span><span class="sxs-lookup"><span data-stu-id="39aeb-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**client memory**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-125">在用戶端電腦) 儲存程式變數的主要記憶體 (。</span><span class="sxs-lookup"><span data-stu-id="39aeb-125">The main memory (where program variables are stored) of the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**剪輯座標**</span><span class="sxs-lookup"><span data-stu-id="39aeb-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**clip coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-127">接下來的座標系統會依照投射矩陣進行轉換，然後在透視區之前。</span><span class="sxs-lookup"><span data-stu-id="39aeb-127">The coordinate system that follows transformation by the projection matrix and precedes perspective division.</span></span> <span data-ttu-id="39aeb-128">視圖-磁片區裁剪是在剪切座標中完成，但應用程式特定的剪輯則否。</span><span class="sxs-lookup"><span data-stu-id="39aeb-128">View-volume clipping is done in clip coordinates, but application-specific clipping is not.</span></span> <span data-ttu-id="39aeb-129">另請參閱 [應用程式特定的剪輯](a.md)。</span><span class="sxs-lookup"><span data-stu-id="39aeb-129">See also [application-specific clipping](a.md).</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**裁剪**</span><span class="sxs-lookup"><span data-stu-id="39aeb-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**clipping**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-131">消除裁剪平面所定義之半形以外的幾何基本物件部分。</span><span class="sxs-lookup"><span data-stu-id="39aeb-131">Eliminating the portion of a geometric primitive that is outside the half-space defined by a clipping plane.</span></span> <span data-ttu-id="39aeb-132">只有在外部時，才會拒絕點。</span><span class="sxs-lookup"><span data-stu-id="39aeb-132">Points are simply rejected if outside.</span></span> <span data-ttu-id="39aeb-133">將會排除一半空格以外的線條或多邊形的部分，並視需要產生額外的頂點，以在裁剪的一半空間內完成基本。</span><span class="sxs-lookup"><span data-stu-id="39aeb-133">The portion of a line or of a polygon that is outside the half-space is eliminated, and additional vertices are generated as necessary to complete the primitive within the clipping half-space.</span></span> <span data-ttu-id="39aeb-134">幾何基本專案和目前的點陣位置 (當指定的) 一律會針對視圖音量的左邊、右邊、下、上、近端和目前平面所定義的六個空格進行裁剪。</span><span class="sxs-lookup"><span data-stu-id="39aeb-134">Geometric primitives and the current raster position (when specified) are always clipped against the six half-spaces defined by the left, right, bottom, top, near, and far planes of the view volume.</span></span> <span data-ttu-id="39aeb-135">應用程式可以指定選擇性的應用程式特定裁剪平面，以套用於眼睛座標中。</span><span class="sxs-lookup"><span data-stu-id="39aeb-135">Applications can specify optional application-specific clipping planes to be applied in eye coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**色彩索引**</span><span class="sxs-lookup"><span data-stu-id="39aeb-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**color index**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-137">表示依名稱的色彩，而不是依值的單一值。</span><span class="sxs-lookup"><span data-stu-id="39aeb-137">A single value that represents a color by name, rather than by value.</span></span> <span data-ttu-id="39aeb-138">OpenGL 色彩索引會視為連續值 (例如，浮點數) ，而運算（例如插補和遞色）則會在其上執行。</span><span class="sxs-lookup"><span data-stu-id="39aeb-138">OpenGL color indexes are treated as continuous values (for example, floating-point numbers) while operations such as interpolation and dithering are performed on them.</span></span> <span data-ttu-id="39aeb-139">不過，儲存在框架緩衝區中的色彩索引一律為整數值。</span><span class="sxs-lookup"><span data-stu-id="39aeb-139">Color indexes stored in the frame buffer are always integer values, however.</span></span> <span data-ttu-id="39aeb-140">浮點數索引會四捨五入為最接近的整數值，以轉換成整數。</span><span class="sxs-lookup"><span data-stu-id="39aeb-140">Floating-point indexes are converted to integers by rounding to the nearest integer value.</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**色彩索引模式**</span><span class="sxs-lookup"><span data-stu-id="39aeb-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**color-index mode**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-142">OpenGL 內容的模式，其中的色彩緩衝區會儲存色彩索引，而不是紅色、綠色、藍色和 Alpha 色彩的元件。</span><span class="sxs-lookup"><span data-stu-id="39aeb-142">Mode of an OpenGL context in which its color buffers store color indexes, rather than red, green, blue, and alpha color components.</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**色彩地圖**</span><span class="sxs-lookup"><span data-stu-id="39aeb-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**color map**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-144">顯示硬體所存取之索引至 RGB 對應的資料表。</span><span class="sxs-lookup"><span data-stu-id="39aeb-144">A table of index-to-RGB mappings that is accessed by the display hardware.</span></span> <span data-ttu-id="39aeb-145">每個色彩索引都會從色彩緩衝區讀取，並在顏色對應中透過查閱轉換成 RGB 三重，並傳送至監視器。</span><span class="sxs-lookup"><span data-stu-id="39aeb-145">Each color index is read from the color buffer, converted to an RGB triple by lookup in the color map, and sent to the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**元件**</span><span class="sxs-lookup"><span data-stu-id="39aeb-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-147">單一、連續的 (例如，代表濃度或數量的浮點) 值。</span><span class="sxs-lookup"><span data-stu-id="39aeb-147">A single, continuous (for example, floating-point) value that represents an intensity or quantity.</span></span> <span data-ttu-id="39aeb-148">通常，元件值為零代表最小值或濃度，而元件值為1代表最大值或濃度，不過有時候會使用其他正規化。</span><span class="sxs-lookup"><span data-stu-id="39aeb-148">Usually, a component value of zero represents the minimum value or intensity, and a component value of one represents the maximum value or intensity, though other normalizations are sometimes used.</span></span> <span data-ttu-id="39aeb-149">由於元件值會在正規化的範圍內轉譯，因此它們會與實際的解析度分開指定。</span><span class="sxs-lookup"><span data-stu-id="39aeb-149">Because component values are interpreted in a normalized range, they are specified independently of actual resolution.</span></span> <span data-ttu-id="39aeb-150">例如，RGB 三 (1，1，1) 是白色，不論色彩緩衝區儲存的是4、8或12位。</span><span class="sxs-lookup"><span data-stu-id="39aeb-150">For example, the RGB triple (1, 1, 1) is white, regardless of whether the color buffers store 4, 8, or 12 bits each.</span></span> <span data-ttu-id="39aeb-151">範圍外的元件通常會壓制至正規化範圍，而不會被截斷或以其他方式轉譯。</span><span class="sxs-lookup"><span data-stu-id="39aeb-151">Out-of-range components are typically clamped to the normalized range, not truncated or otherwise interpreted.</span></span> <span data-ttu-id="39aeb-152">例如，RGB 三 (1.4、1.5、0.9) 壓制為 (1.0、1.0、0.9) ，然後再用來更新色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="39aeb-152">For example, the RGB triple (1.4, 1.5, 0.9) is clamped to (1.0, 1.0, 0.9) before it's used to update the color buffer.</span></span> <span data-ttu-id="39aeb-153">紅色、綠色、藍色、Alpha 和深度一律會被視為元件，而不是索引。</span><span class="sxs-lookup"><span data-stu-id="39aeb-153">Red, green, blue, alpha, and depth are always treated as components, never as indexes.</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**上下文**</span><span class="sxs-lookup"><span data-stu-id="39aeb-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-155">一組完整的 OpenGL 狀態變數。</span><span class="sxs-lookup"><span data-stu-id="39aeb-155">A complete set of OpenGL state variables.</span></span> <span data-ttu-id="39aeb-156">請注意，畫面格緩衝區內容不是 OpenGL 狀態的一部分，但畫面格緩衝區的設定為。</span><span class="sxs-lookup"><span data-stu-id="39aeb-156">Note that framebuffer contents are not part of the OpenGL state, but that the configuration of the framebuffer is.</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**凸**</span><span class="sxs-lookup"><span data-stu-id="39aeb-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**convex**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-158">多邊形的條件，在多邊形的平面中，沒有任何直線與多邊形相交兩倍以上。</span><span class="sxs-lookup"><span data-stu-id="39aeb-158">Condition of a polygon in which no straight line in the plane of the polygon intersects the polygon more than twice.</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**凸殼**</span><span class="sxs-lookup"><span data-stu-id="39aeb-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**convex hull**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-160">封閉指定點群組的最小凸區域。</span><span class="sxs-lookup"><span data-stu-id="39aeb-160">The smallest convex region enclosing a specified group of points.</span></span> <span data-ttu-id="39aeb-161">在兩個維度中，凸殼在概念上是藉由在點周圍延展橡皮線來找出，讓所有點都落在頻內。</span><span class="sxs-lookup"><span data-stu-id="39aeb-161">In two dimensions, the convex hull is found conceptually by stretching a rubber band around the points so that all of the points lie within the band.</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**座標系統**</span><span class="sxs-lookup"><span data-stu-id="39aeb-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**coordinate system**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-163">在 n 維度空間中，一組 n 個線性獨立的向量，而且錨定某個點 (稱為原點)。</span><span class="sxs-lookup"><span data-stu-id="39aeb-163">In n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="39aeb-164">座標群組會指定 spaceIn n 維度空間中的點，這是一組指向點 (的 n 個線性獨立向量，稱為「原始) 」。</span><span class="sxs-lookup"><span data-stu-id="39aeb-164">A group of coordinates specifies a point in spaceIn n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="39aeb-165">一組座標會指定空間中的某個點 (或是從原點算起的向量)，方法是指出要沿著每一個向量行進多遠才能到達此點 (或是向量的尖端)。</span><span class="sxs-lookup"><span data-stu-id="39aeb-165">A group of coordinates specifies a point in space (or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span> <span data-ttu-id="39aeb-166">從原點) 的 (或向量，指出每個向量的行進距離，以達到向量)  (或刀尖的位置。</span><span class="sxs-lookup"><span data-stu-id="39aeb-166">(or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**撲殺**</span><span class="sxs-lookup"><span data-stu-id="39aeb-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**culling**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-168">消除多邊形正面或背面的程式，讓臉部不會繪製。</span><span class="sxs-lookup"><span data-stu-id="39aeb-168">The process of eliminating a front face or back face of a polygon so that the face isn't drawn.</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**目前的矩陣**</span><span class="sxs-lookup"><span data-stu-id="39aeb-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**current matrix**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-170">將一個座標系統中的座標轉換成另一個系統座標的矩陣。</span><span class="sxs-lookup"><span data-stu-id="39aeb-170">A matrix that transforms coordinates in one coordinate system to coordinates of another system.</span></span> <span data-ttu-id="39aeb-171">OpenGL 中有三個目前的矩陣：模型矩陣，此矩陣會將程式設計人員) 指定的座標 (座標轉換為眼睛座標;將眼睛座標轉換成剪切座標的透視圖矩陣;和材質矩陣，會轉換指定或產生的材質座標（如同矩陣所述）。</span><span class="sxs-lookup"><span data-stu-id="39aeb-171">There are three current matrices in OpenGL: the modelview matrix, which transforms object coordinates (coordinates specified by the programmer) to eye coordinates; the perspective matrix, which transforms eye coordinates to clip coordinates; and the texture matrix, which transforms specified or generated texture coordinates as described by the matrix.</span></span> <span data-ttu-id="39aeb-172">每個目前的矩陣都是矩陣堆疊上的最上層元素。</span><span class="sxs-lookup"><span data-stu-id="39aeb-172">Each current matrix is the top element on a stack of matrices.</span></span> <span data-ttu-id="39aeb-173">這三個堆疊中的每一個都可以使用 OpenGL 矩陣操作命令來操作。</span><span class="sxs-lookup"><span data-stu-id="39aeb-173">Each of the three stacks can be manipulated with OpenGL matrix-manipulation commands.</span></span>

</dd> <dt>

<span data-ttu-id="39aeb-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**目前的點陣位置**</span><span class="sxs-lookup"><span data-stu-id="39aeb-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**current raster position**</span></span>
</dt> <dd>

<span data-ttu-id="39aeb-175">視窗座標位置，指定影像基本的位置（當影像成為柵格化時）。</span><span class="sxs-lookup"><span data-stu-id="39aeb-175">A window coordinate position that specifies the placement of an image primitive when it's rasterized.</span></span> <span data-ttu-id="39aeb-176">呼叫 glRasterpos 時，會更新目前的點陣位置和其他目前的點陣參數。</span><span class="sxs-lookup"><span data-stu-id="39aeb-176">The current raster position, and other current raster parameters, are updated when glRasterpos is called.</span></span>

</dd> </dl>

 

 




