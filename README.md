import math

# Öklid mesafesini hesaplayan fonksiyon
def euclideanDistance(point1, point2):
    return math.sqrt((point2[0] - point1[0])**2 + (point2[1] - point1[1])**2)

# Noktaların tanımlanması
points = [(1, 2), (4, 6), (5, 3), (2, 8), (9, 10)]

# Mesafeleri saklayacak liste
distances = []

# Tüm nokta çiftleri arasındaki mesafeleri hesaplama
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)

# Minimum mesafenin bulunması
minimum_distance = min(distances)

# Sonuçların yazdırılması
print("Nokta listesi:", points)
print("Tüm noktalar arasındaki mesafeler:", distances)
print("En kısa mesafe:", minimum_distance)
